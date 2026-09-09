# Chapter 4: Design

> Lead: Zakaria (S2) — Co-author: Ahmed (S3). Target: draft by end of Week 9 (M2).

## 4.1 Introduction
[ TBD ]

## 4.2 Database Design
### 4.2.1 Relation Schema
[ TBD: users, patients, doctors, admins, specialties, appointments, consultations,
       diagnoses, prescriptions, health_logs, risk_factors, twin_scores, alerts,
       notifications — mapped from ERD ]
### 4.2.2 Data Dictionary
[ TBD: one table per relation — column, type, null, key, description ]
### 4.2.3 Query Statements
[ TBD: key queries used by reports & dashboard (SQL) ]

## 4.3 System Interface Design
### 4.3.1 Interface Hierarchy
[ TBD: mobile app nav tree + dashboard nav tree ]
### 4.3.2 Main Interfaces
[ TBD: wireframes — login, home, bookings, consultation, health profile, twin page ]
### 4.3.3 Transitional Interfaces
[ TBD: loading/confirmation/empty states ]
### 4.3.4 System Forms
[ TBD: booking form, symptom/progress form, diagnosis form ]
### 4.3.5 System Queries
[ TBD ]
### 4.3.6 System Reports
[ TBD: doctor reports, admin statistics, twin alerts list ]

## 4.4 Digital Twin Engine Specification
> This feeds T26 (backend). Define formulas and decision tables here — see AGENTS.md §8.
### 4.4.1 Risk Categories & Weights
[ TBD: risk factors, chronic conditions, symptom severity, medication conflicts, adherence ]
### 4.4.2 Composite Risk Index Formula (0–100)
[ TBD: weighted sum + normalization ]
### 4.4.3 Treatment-Response Trend
[ TBD: compare symptom scores before/after diagnosis over time ]
### 4.4.4 Rule Table (Recommendations / Alerts)
[ TBD: IF-THEN table ]

## 4.5 API Design (contract for integration)
[ TBD: endpoints, methods, requests/responses — feeds Ch5/task T27 ]