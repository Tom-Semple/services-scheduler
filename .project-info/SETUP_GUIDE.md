# Lawn Service Scheduler - Cursor IDE Setup Guide
## Build Your Focused Lawn Service Platform with AI

Based on analysis of your existing codebase, here's a step-by-step guide to rebuild your scheduler with Cursor IDE.

---

## 🚀 **Initial Project Setup**

### **Step 1: Create New Project**
```bash
npx create-vite@latest lawn-scheduler --template react-ts
cd lawn-scheduler
npm install
```

### **Step 2: Install Core Dependencies**
Tell Cursor: 
> "Install these exact dependencies for my lawn service scheduler: @supabase/supabase-js, @radix-ui/react-dialog, @radix-ui/react-select, @radix-ui/react-checkbox, class-variance-authority, clsx, tailwind-merge, lucide-react, react-router-dom, sonner, date-fns, react-hook-form, @hookform/resolvers, zod, twilio"

### **Step 3: Setup Tailwind with Custom Colors**
Tell Cursor:
> "Setup Tailwind CSS with a custom red, black, white theme. Primary red should be #dc2626, secondary black #000000, with white backgrounds. Configure tailwind.config.js with these custom colors and make sure all component styling uses these theme colors."

---

## 🎨 **Design System Setup**

### **Step 4: Create Simple Design System**
Tell Cursor:
> "Create a simple design system file at src/styles/theme.css with CSS custom properties for red (#dc2626), black (#000000), and white (#ffffff) colors. Include button styles, card styles, and form styles using these colors. Keep it minimal - no gradients, no fancy effects, just clean red/black/white styling."

### **Step 5: Setup Component Structure**
Tell Cursor:
> "Create this exact folder structure in src/:
- components/
  - ui/ (basic button, input, dialog, card components)
  - customers/
  - properties/  
  - jobs/
  - contractors/
- hooks/
- pages/
- services/
- types/
- utils/"

---

## 🗄️ **Database & Backend Setup**

### **Step 6: Supabase Configuration**
Tell Cursor:
> "Create Supabase client configuration at src/lib/supabase.ts using my existing Supabase project. Then create these exact table types in src/types/database.ts based on my current schema: Customer, Property, Job, Contractor. Keep types simple with only essential fields."

### **Step 7: Database Schema**
**Use your existing Supabase tables but tell Cursor:**
> "Create SQL migration to add these columns to my existing jobs table: territory (text), required_equipment (text array), weather_dependent (boolean), auto_assigned (boolean). Also create a new contractors table with: id, name, phone, territories (text array), skills (text array), active (boolean)."

---

## 🔧 **Core Functionality Build**

### **Step 8: Customer Management**
Tell Cursor:
> "Build simple customer management with a hook useCustomers.ts that handles CRUD operations. Create a customers page with a clean table view and an add customer dialog. Use red buttons, simple white cards, black text. No fancy animations - just functional."

### **Step 9: Property Management** 
Tell Cursor:
> "Build property management linked to customers. Each property has name, address, customer_id, and terrain_type. Create a simple properties page with search and add property dialog. Keep the same red/black/white theme."

### **Step 10: Contractor Management**
Tell Cursor:
> "Create contractor management system. Contractors have name, phone, territories array (North, South, East, West), and skills array (Lawn Cutting, Hedge Trimming, etc). Simple CRUD interface with red/black/white styling."

---

## ⚡ **Smart Job Scheduling**

### **Step 11: Job Creation System**
Tell Cursor:
> "Build job scheduling system with auto-assignment. When creating a job, auto-select contractor based on property territory and contractor skills. Include equipment checklist based on job type (Lawn Cutting = Mower + Strimmer, etc). Use simple dropdowns and checkboxes."

### **Step 12: One-Click Scheduling**
Tell Cursor:
> "Create a dashboard with quick scheduling widget. Customer autocomplete → property dropdown → job type → date picker → auto-assigns contractor → creates job. All in one simple form with red submit button."

### **Step 13: Calendar View**
Tell Cursor:
> "Build simple calendar view showing all scheduled jobs. Use a basic monthly calendar with job dots. Click job to see details. Red theme, white background, black text."

---

## 📱 **Communication System**

### **Step 14: SMS Integration**
Tell Cursor:
> "Setup Twilio SMS service at src/services/sms.ts. Create sendJobNotification function that sends simple text: 'NEW JOB: [job type] at [address] on [date]. Equipment: [list]. Details: [link]'. Trigger automatically when job is assigned."

### **Step 15: Weather Integration**
Tell Cursor:
> "Add weather API integration using WeatherAPI.com. Check weather for job dates and show warning if rain expected. Simple weather widget on dashboard showing today's conditions."

---

## 🔗 **Job Information System**

### **Step 16: Unique Job Links**
Tell Cursor:
> "Create unique job information system. Generate secure URLs for each job (job/[token]) that shows customer info, property details, and instructions without login. Add simple status update form on same page."

### **Step 17: Job Status Tracking**
Tell Cursor:
> "Build job status tracking. Contractors can update status via unique links. Simple dropdown: Not Started → In Progress → Completed. Comments field and photo upload. Updates visible on admin dashboard."

---

## 📊 **Dashboard & Overview**

### **Step 18: Admin Dashboard** 
Tell Cursor:
> "Create clean admin dashboard showing: today's jobs, weather widget, contractor status (how many jobs each has), and the one-click scheduling widget. Use simple white cards with red accents and black text."

### **Step 19: Equipment Tracking**
Tell Cursor:
> "Add equipment management. Track Mowers, Strimmers, Tools by location (Warehouse, With John, With Mike, etc). Simple table view with status updates."

---

## 🔧 **Polish & Finishing**

### **Step 20: Navigation & Layout**
Tell Cursor:
> "Create simple sidebar navigation with: Dashboard, Customers, Properties, Jobs, Contractors, Equipment. Red sidebar with white text. Clean, minimal design. Mobile responsive hamburger menu."

### **Step 21: Error Handling & Loading States**
Tell Cursor:
> "Add simple loading spinners and error messages throughout the app. Use red spinners and error text. Toast notifications for success/error actions using sonner library."

### **Step 22: Environment Setup**
Tell Cursor:
> "Setup environment variables for Supabase URL/Key, Twilio credentials, and Weather API key. Create .env.example file with all required variables."

---

## 📋 **Key Cursor Prompts for Each Step**

### **For Every Component Request:**
> "Keep this component extremely simple. Use red (#dc2626) for primary actions, black (#000000) for text, white (#ffffff) for backgrounds. No fancy animations, gradients, or effects. Just clean, functional design. Make all colors easy to change via CSS variables."

### **For Every Feature Request:**
> "Write the minimum code needed for this feature to work. No over-engineering, no complex abstractions. Simple functions, clear variable names, direct implementation."

### **For Styling Requests:**
> "Use CSS custom properties for all colors so they can be easily changed. All styling should be in CSS files, not inline or in Tailwind classes. Red buttons, white cards, black text, minimal design."

---

## 🎯 **Testing Your Build**

### **Step 23: Core Workflow Test**
Test this exact workflow:
1. Add customer → Add property → Schedule job → Check auto-assignment → Verify SMS sent → Update job status via link

### **Step 24: Data Flow Test**
Verify: Customer creation → Property linking → Job scheduling → Contractor assignment → SMS notification → Status updates

---

## ⚡ **Deployment Prep**

### **Step 25: Build Optimization**
Tell Cursor:
> "Optimize the build for production. Remove any unused dependencies, ensure all environment variables are properly configured, and create simple deployment documentation."

### **Step 26: Documentation**
Tell Cursor:
> "Create simple README with setup instructions, environment variables needed, and basic usage guide. Keep it minimal but complete."

---

## 🚨 **Critical Success Criteria**

After following this guide, you should have:
- ⚡ **15-second job scheduling** from dashboard
- 🎯 **Automatic contractor assignment** based on territory
- 📱 **SMS notifications** sent automatically
- 🌤️ **Weather warnings** for outdoor jobs
- 🔗 **Unique job links** for contractor access
- 🎨 **Consistent red/black/white theme** throughout
- 📝 **Clean, simple code** that's easy to modify

---

## 💡 **Pro Tips for Cursor Usage**

1. **Be Specific**: Always mention "red/black/white theme" and "simple/minimal design"
2. **Reference Your Current App**: Say "like my existing app but simpler"
3. **One Feature at a Time**: Don't ask for multiple features in one prompt
4. **Test as You Go**: Build and test each step before moving to the next
5. **Keep It Simple**: Always emphasize simplicity and minimal code

This guide will give you a focused, clean lawn service scheduler in a fraction of the time it would take to refactor your existing codebase.