# E-Commerce System Design Task

This repository contains my solution for a medium-sized e-commerce system design task.

The goal is to design a platform that:

- synchronizes products and categories from a third-party supplier,
- allows users to search products, add them to a cart, and checkout,
- validates product data before order confirmation.

## Included Materials

- Architecture Diagram
- BPMN Diagram
- ERD Diagram
- Detailed Documentation
- Risks and Edge Cases
- User Stories

## Scope

### Functional
- Synchronize products and categories from supplier API
- Search products
- Add products to cart
- Checkout and create orders

### Non-Functional
- Keep checkout data as consistent as possible
- Keep user flows fast and responsive

### Out of Scope
- Notifications
- Order cancellation / refunds
- Delivery tracking
- Full user management

## Architecture Overview

The solution is designed as a **modular monolith** with a **shared PostgreSQL database**.

Main modules:
- Catalog Sync & Validation
- Search
- Cart
- Orders

This approach keeps the system simple for MVP while preserving clear module boundaries.

## Key Design Decisions

- Supplier data is synchronized into a **local catalog**
- Search and browsing use **local database data**
- Checkout includes **product revalidation**
- Product availability means **existence in supplier catalog**
- Quantity-based stock validation is **out of scope**
- Order data stores **price and contact snapshots** for historical correctness

## Main Risks Considered

- stale product data during checkout
- supplier API unavailability
- duplicate checkout requests
- parallel checkout on the same product
- failed or partial sync runs

## Suggested Structure

├── README.md
├── docs
├── diagrams
