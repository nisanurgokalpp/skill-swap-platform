# Skill Swap Platform

## Architectural Style Selection (Sprint A)

For the Skill Swap Platform, we have adopted a hybrid architectural style combining **Layered Architecture** and **MVC (Model-View-Controller)**. 

The primary quality attributes driving this decision are **maintainability** and **testability**. A Layered Architecture allows us to strictly separate the presentation layer, business logic, and data access layer. This ensures that any future changes to the database schema or external APIs will only affect the data access layer, preventing a ripple effect across the system and making unit testing much easier.

Additionally, integrating the MVC pattern provides a clean separation between the user interface (View), the core business rules (Model), and the routing logic (Controller). While this layered approach may introduce a slight performance overhead compared to a monolithic structure, the trade-off is highly favorable for our system. For a platform matching users and managing skills, data consistency and long-term modifiability are significantly more critical than microsecond-level performance optimizations.