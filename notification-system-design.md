# Notification System Design
### Stage 1
    Priority Algorithm: Unread notifications are ranked using a strict priority hierarchy based on Placement, Result, Event, and Recency (timestamp).
    Weight Calculation: Categorical fields are converted to numeric scores to evaluate and sort the top 10 notifications deterministically without database support.
    Stream Optimization: To handle a live influx of new notifications efficiently, the system avoids costly full-array sorting algorithms.
