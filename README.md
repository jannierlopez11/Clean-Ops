# Cleaning Ops

Cleaning Ops is a mobile-first restaurant cleaning operations app designed to manage employees, restaurant assignments, cleaning checklists, photos, time tracking, signatures, and work history in one place.

## Core Features

### Manager
Managers can:
- View the employee database
- Search employees
- View employee profiles
- Assign employees to restaurants
- Remove restaurant assignments
- Activate or deactivate employees
- View restaurants
- Edit restaurant information
- Manage cleaning operations
- Review completed work
- Review employee hours
- Review job photos
- Review checklist completion

### Employee
Employees can:
- Create their own account
- View assigned restaurants
- Clock in and out
- Complete cleaning checklists
- Upload before/after photos
- Sign completed jobs
- View their own work

## Restaurant Schedule

| Day | Restaurant | Time |
|---|---|---|
| Monday | Covington | 4:00 AM |
| Tuesday | Highland | 5:00 AM |
| Wednesday | East | 5:00 AM |
| Thursday | Lafayette | 4:00 AM |
| Friday | Parrains | 5:00 AM |

## Cleaning Checklist

The checklist is organized by category, equipment, and individual cleaning points.

### Kitchen Equipment
Includes:
- Gas Range
- Burners
- Grates
- Grease Trays
- Knobs
- Front, sides, back and bottom
- Flat Top / Griddle
- Charbroiler
- Gas Grill
- Salamander / Broiler
- Fryers
- Fryer Filter Machine
- Pressure Fryer
- Steam Table
- Hot Holding Cabinet
- Convection Oven
- Baking Oven
- Pizza Oven
- Deck Oven
- Combi Oven
- TurboChef / Rapid Cook Oven
- Commercial Mixer
- Food Processor
- Meat Slicer
- Meat Grinder
- Vegetable Cutter / Chopper
- Commercial Blender
- Rice Cooker
- Rice Warmer
- Food Warmer
- Microwave
- Panini Press
- Waffle Maker
- Toaster
- Conveyor Toaster
- Proofing Cabinet
- Soup Warmer
- Coffee Machine

### Refrigeration
Each refrigeration unit is tracked separately.

- Walk-In Refrigerator
- Walk-In Freezer
- Reach-In Refrigerator
- Reach-In Freezer
- Under-Counter Refrigerator
- Prep Refrigerator
- Refrigerated Prep Table
- Ice Machine
- Ice Storage Bin
- Bar Ice Machine

### Washing Area
- Commercial Dishwasher
- Dishwashing Sink
- Pre-Rinse Station
- Three-Compartment Sink
- Handwashing Sink
- Mop Sink
- Garbage Disposal

### Tables & Surfaces
- Prep Tables
- Cutting Boards
- Stainless Steel Prep Tables
- Shelving
- Storage Racks
- Food Storage Cabinets

Prep tables can include:
- Top
- Bottom
- Legs
- Edges
- Corners
- Drawers
- Shelves
- Wall behind
- Floor underneath

### Ventilation
- Exhaust Hood
- Hood Filters
- Exhaust Fans
- Ventilation Covers
- Accessible Air Duct Areas

### Floors & Structure
- Kitchen Floors
- Dining Room Floors
- Bar Floors
- Patio Floors
- Floor Drains
- Floor Mats
- Baseboards
- Wall Edges
- Kitchen Walls
- Dining Room Walls
- Bar Walls
- Accessible Ceiling Areas
- Wooden Ceiling Areas

### Bar / Beverage Area
- Beverage Prep Tables
- Beverage Machine
- Beverage Dispenser
- Soda Fountain
- Blender Station
- Coffee Station
- Beer Service Area
- Bar Sink
- Bar Refrigerators
- Bar Freezers
- Bar Ice Machine
- Bar Shelving
- Bar Drawers / Cabinets

### Trash & Exterior
- Trash Cans
- Dumpster Area
- Dumpster Pad
- Trash Compactor
- Grease Trap inspection/reminder
- Outdoor Grill
- Outdoor Cooking Equipment
- Exterior Walls
- Exterior Doors
- Patio Area
- Entry Area

## Bathrooms

Bathrooms are **mandatory every service day**.

They are NOT part of the weekly rotation.

The system supports:
- Toilets
- Urinals
- Sinks
- Faucets
- Mirrors
- Soap Dispensers
- Paper Towel Dispensers
- Hand Dryers
- Bathroom Floors
- Walls
- Doors
- Door Handles
- Trash Cans
- Baseboards
- Vents
- High-Touch Areas
- Supplies Check

Multiple toilets, urinals, and sinks can be configured for each bathroom.

## Database

Cleaning Ops uses Supabase for persistent data.

Main tables include:

- `profiles`
- `restaurants`
- `employee_assignments`
- `checklist_categories`
- `checklist_items`
- `checklist_subtasks`
- `restaurant_checklist_items`
- `restaurant_bathrooms`
- `cleaning_rotations`
- `checklist_tasks`
- `time_entries`
- `job_photos`
- `completion_signatures`
- `notifications`
- `task_templates`

## Authentication

Employees can create their own accounts using:

- Full name
- Email
- Password
- Password confirmation

New employee accounts automatically receive an employee profile.

Manager permissions are controlled through roles and Supabase security policies.

## Photos

Job photos are stored in the private `job-photos` Supabase Storage bucket.

The system is designed for:

- Before photos
- After photos
- Restaurant-specific job photos
- Manager photo review

## User Interface

Cleaning Ops uses a professional mobile-first design.

### Design
- Navy
- Black
- Gold
- Subtle dark red accents
- Cream/light typography
- Compact cards
- Rounded controls
- Clean spacing
- Professional operations-dashboard style

The main menu is a simple **three horizontal line icon in the top-right corner**.

The menu should not use a gear icon or emoji.

## Languages

The app supports:

- English
- Español

## Manager Structure

The planned management hierarchy is:

**Owner**
→ **Managers**
→ **Employees**

The Owner will have control over managers.

Managers will manage employees, restaurants, assignments, and daily operations.

Employees will only have access to their own assigned work.

## Security

Never place a Supabase secret or service-role key in the frontend or GitHub repository.

Only the public/publishable Supabase key should be used by the browser.

Supabase Row Level Security and Storage policies should protect:

- Employee data
- Restaurant data
- Assignments
- Checklist records
- Time entries
- Photos
- Signatures

Manager-only actions must be protected by database permissions, not just hidden frontend buttons.

## Development Roadmap

### Completed Foundation
- Supabase connection
- Authentication
- Employee self-signup
- Employee profiles
- Restaurant database
- Employee assignments
- Detailed checklist database
- Bathroom configuration
- Cleaning rotation foundation
- Photo storage
- Time tracking foundation
- Notifications foundation
- GitHub Pages deployment

### Current Development
- Unified Manager dashboard
- Employee dashboard
- Employee database
- Employee profiles
- Restaurant management
- Detailed checklist interface
- Mobile-first redesign
- Three-line top-right menu

### Upcoming
- Full restaurant checklist editor
- Bathroom configuration editor
- Employee work history
- Employee hour reports
- Completed checklist history
- Photo gallery
- Completion signatures
- Manager reports
- Owner/Manager controls
- Complete English/Spanish translation

## Deployment

Cleaning Ops is deployed through GitHub Pages.

Live application:

https://jannierlopez11.github.io/Clean-Ops/

Repository:

jannierlopez11/Clean-Ops

## Version

Current development version: **v7**

Cleaning Ops is being developed as a real Supabase-backed application rather than a browser-only demo.

---

**Cleaning Ops**  
*Restaurant cleaning operations, organized in one place.*
