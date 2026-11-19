This is the git repo to keep track of Time series data analysis

### Missing Data Treatment

Missing daily mean temperature observations were imputed separately for Vancouver, Toronto, and Winnipeg using a structural state-space model and Kalman smoothing. To account for annual seasonality and long-term warming, each station's daily temperature series was first modeled using a linear trend and two Fourier harmonics. A local-level state-space model was then fitted to the remaining residuals, and Kalman smoothing was applied to estimate missing observations. Original observed temperatures were preserved.

Following imputation, weekly mean temperatures were calculated using all seven daily values for each Monday–Sunday week. Weeks were assigned to calendar years according to their Thursday midpoint. This approach recovered weeks previously excluded due to missing observations while retaining the natural variation of 52 or 53 weeks per year.

The estimated warming rates changed only slightly following imputation, suggesting that the overall long-term warming conclusions were relatively insensitive to the missing-data treatment. However, imputed temperatures remain model-based estimates, and associated uncertainty is not explicitly incorporated into the subsequent annual trend regression.
