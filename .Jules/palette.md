## 2026-11-11 - Added missing tooltips, input labels, and aria-live status
**Learning:** Icon-only buttons often have aria-labels but sighted users miss out on native tooltips. Chat textareas often rely on placeholders, making them less accessible. Status indicators missing aria-live don't announce async loading state to screen readers.
**Action:** Always add 'title' mirroring 'aria-label' on icon-only buttons. Ensure main inputs like textareas have explicit aria-labels. Add aria-live="polite" to async loading states (#working).
