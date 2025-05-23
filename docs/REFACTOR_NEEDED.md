
# Refactoring Needed

This document outlines files and components that require refactoring for better maintainability.

## High Priority Files

1. **AppSidebar.tsx (219 lines)**
   - Split into smaller components:
     - SidebarNav (created)
     - SidebarHeader
     - SidebarFooter
   - Migrate navigation items to a separate configuration file
   - Status: ✅ Refactored

2. **TeamDetail.tsx (262 lines)**
   - Break into smaller components:
     - TeamDetailHeader
     - TeamDetailTabs
     - TeamStats
     - PlayerList
   - Extract repeated UI patterns into reusable components
   - Status: ⚠️ Partially refactored

3. **Teams.tsx (375 lines)**
   - Extract list rendering logic to separate component
   - Create TeamListFilters component
   - Separate team comparison logic
   - Status: ⚠️ Started but needs more work

4. **Analysis.tsx (329 lines)**
   - Extract chart components
   - Create separate analysis tabs components
   - Create reusable metric display components
   - Status: ❌ Not started

5. **Matches.tsx (374 lines)**
   - Extract match list component
   - Create match detail viewer component
   - Separate filter controls
   - Status: ❌ Not started

## Medium Priority Files

6. **Dashboard.tsx**
   - Extract dashboard widgets into separate components
   - Create a layout system for dashboard widgets
   - Status: ❌ Not started

7. **NotFound.tsx**
   - No major refactoring needed, but could extract error display to reusable component
   - Status: ✅ Good condition

8. **Sidebar.tsx**
   - Replace with new SidebarNav component
   - Status: ✅ Replaced

## Lower Priority Files

9. **Header.tsx**
   - Extract navigation items to configuration file
   - Create separate component for user menu
   - Status: ⚠️ Needs improvement

10. **LeagueManagement.tsx**
    - Extract stats cards to reusable component
    - Create form components for league management
    - Status: ❌ Not started

## General Refactoring Guidelines

1. **Component Size Limit**: Keep components under 100 lines
2. **Single Responsibility**: Each component should do one thing well
3. **Props Interface**: Always define TypeScript interfaces for component props
4. **Responsive Design**: Ensure all components work on mobile devices
5. **Error Handling**: Add proper error boundaries and loading states
6. **Performance**: Add memo/useMemo for expensive renders/calculations
7. **Accessibility**: Ensure all components are keyboard navigable and have proper aria attributes
