commit 4727fb5038add090842d618ef2ccbca5303fdb20
Author: Nikolay Deshev <nikolay.deshev@sap.com>
Date:   Fri May 1 09:58:21 2026 +0300

    refactor(ui5-range-slider): refactor ui5-range-slider component (#13316)
    
    * feat(ui5-range-slider): refactor ui5-range-slider component
    
    Extracted reusable SliderHandle and SliderScale components from
    RangeSlider for better modularity and code reuse with Slider
    Refactored RangeSliderTemplate to use composition with the new
    sub-components instead of inline markup
    Added progress bar ARIA and focus properties to SliderScale to support
    RangeSlider's range selection feature
    Consolidated and cleaned up CSS theme parameters across all themes
    (Horizon, Fiori 3, HCB/HCW variants)
    Removed aria-keyshortcuts attributes from the handles to avoid duplicated speech output
    Removed the wrong aria-describedby references
    Fixes various minor issues
    
    FIXES: #13348
