# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a comprehensive **Sheep Farming Financial Feasibility Calculator** built as a single-page HTML application. The calculator is designed specifically for the Egyptian market and provides detailed financial analysis for sheep farming operations.

## Application Structure

The application is a single `index.html` file containing:

- **Arabic RTL interface** - All text and layout is in Arabic with right-to-left direction
- **Tabbed interface** with 11 main sections:
  1. Market Research (بحث السوق)
  2. Livestock Data (بيانات الأغنام) 
  3. Infrastructure (البنية التحتية)
  4. Operations (التشغيل)
  5. Breeding Program (برنامج التربية)
  6. Risks & Taxes (المخاطر والضرائب)
  7. Seasonal Analysis (التحليل الموسمي)
  8. Financial Analysis (التحليل المالي)
  9. Multi-Year Planning (التخطيط متعدد السنوات)
  10. Feed Optimizer (محسن الأعلاف)
  11. Breeding Calendar (تقويم التربية)
  12. Sensitivity Analysis (تحليل الحساسية)

## Key Features

### Core Financial Analysis
- **Comprehensive financial modeling** covering all aspects of sheep farming
- **Real-time calculations** that update as users input data
- **Multi-revenue stream analysis** including sacrificial animals, meat sales, catering, live animal sales, exports, manure, and hide sales
- **Risk assessment** with mortality rates, feed price volatility, and emergency reserves
- **Seasonal analysis** for cash flow planning
- **Islamic finance compliance** with automatic Zakat calculations
- **Egyptian market specifics** including local prices, regulations, and market conditions

### Advanced Features Added
- **Data Management System** - Save/load projects, export to PDF/Excel, print functionality
- **Visual Analytics** - Interactive charts using Chart.js for cash flow, revenue distribution, break-even analysis
- **Multi-Year Planning** - 5-year financial projections with flock growth modeling and expansion planning
- **Feed Formula Optimizer** - Calculate optimal feed mix for cost/nutrition balance using linear programming concepts
- **Breeding Calendar** - Track breeding seasons, birth schedules, and production timeline
- **Sensitivity Analysis** - Monte Carlo simulation and tornado charts for risk assessment
- **Market Intelligence** - Price trend analysis and competitor comparison tools
- **Compliance Tracker** - Document checklist for permits, certificates, and regulatory requirements

### Interactive Charts & Visualizations
- Monthly cash flow projections
- Revenue stream pie charts
- Break-even analysis graphs
- Cost breakdown visualizations
- Multi-year financial performance
- Flock growth projections
- Feed composition optimization
- Production timeline charts
- Sensitivity tornado diagrams
- Monte Carlo probability distributions

## Technical Implementation

### Core Technologies
- **HTML5/CSS3/JavaScript ES6** - Modern web standards
- **Chart.js** - Interactive data visualization library
- **jsPDF** - PDF generation for reports
- **Responsive design** with mobile-first approach
- **CSS Grid layouts** for complex form arrangements
- **Real-time validation** and automatic calculations
- **Localized number formatting** for Egyptian Arabic
- **Event-driven architecture** for form interactions

### External Dependencies
- Chart.js (CDN): `https://cdn.jsdelivr.net/npm/chart.js`
- jsPDF (CDN): `https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js`

### Data Management
- **Local Storage** - Browser-based project saving
- **JSON Import/Export** - Portable project files
- **CSV Export** - Excel-compatible data export
- **PDF Reports** - Professional presentation format
- **Print Optimization** - Clean printed layouts

## Core Calculation Logic

The main calculation function `calculateAll()` performs complex financial modeling including:

- **Investment calculations** (infrastructure, livestock, working capital)
- **Revenue projections** across multiple streams
- **Operating cost analysis** (feed, labor, veterinary, utilities)
- **Tax and regulatory compliance** (income tax, VAT, Zakat)
- **Break-even analysis** and ROI calculations
- **Seasonal cash flow modeling**

## Styling Guidelines

- **Arabic typography** with proper RTL support
- **Responsive grid systems** for different screen sizes
- **Color-coded sections** for different types of information
- **Professional color scheme** with blue (#3498db) as primary accent
- **Compact mobile layout** optimized for smaller screens

## Data Validation

Input fields include:
- **Automatic calculations** for dependent values
- **Read-only fields** for computed results
- **Reasonable default values** based on Egyptian market conditions
- **Input validation** for logical constraints

## Key Functions and Architecture

### Main Calculation Functions
- `calculateAll()` - Master calculation function that triggers all financial modeling
- `calculateMultiYear()` - 5-year projection calculations with growth factors
- `optimizeFeed()` - Feed formula optimization using simplified linear programming
- `generateBreedingCalendar()` - Creates breeding timeline and schedules
- `runSensitivityAnalysis()` - Monte Carlo simulation and sensitivity analysis
- `runMonteCarloSimulation()` - Statistical risk modeling

### Chart Creation Functions
- `createCharts()` - Main chart initialization
- `createCashFlowChart()` - Monthly cash flow visualization
- `createRevenueChart()` - Revenue distribution pie chart
- `createBreakEvenChart()` - Break-even analysis timeline
- `createSensitivityChart()` - Tornado chart for variable impact
- `createMonteCarloChart()` - Probability distribution histogram

### Data Management Functions
- `saveProject()` - Export project data as JSON
- `loadProject()` - Import project data from JSON file
- `exportToPDF()` - Generate PDF reports using jsPDF
- `exportToExcel()` - Create CSV files for Excel compatibility
- `generateDetailedReport()` - Comprehensive financial report generation

## Development Notes

- All calculations are performed client-side in JavaScript
- No server-side components or database required
- Suitable for deployment as a static website
- Can be easily modified for other markets by updating default values and currencies
- Charts auto-update when switching between tabs
- Modal dialogs for detailed reporting and export options
- Responsive design works on desktop, tablet, and mobile devices
- Print-friendly layouts with CSS media queries

## Common Development Tasks

### Adding New Input Fields
1. Add HTML input element with unique ID
2. Update `calculateAll()` function to read the new value
3. Incorporate into relevant calculations
4. Add to save/load functionality in data management functions

### Adding New Charts
1. Create canvas element in appropriate tab
2. Add chart creation function following existing patterns
3. Call chart function when tab becomes active
4. Handle chart destruction when switching tabs

### Modifying Calculations
1. Locate relevant section in `calculateAll()` function
2. Update formulas while maintaining existing variable names
3. Test with various input scenarios
4. Update display elements to show new results