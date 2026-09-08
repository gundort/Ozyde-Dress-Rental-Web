Ozyde

Smart luxury rental for Mzansi.

Ozyde is a premium dress rental and custom design platform built for the South African market. It connects customers with designer dresses for weddings, matric dances, birthdays, and formal events — making luxury accessible without the cost of ownership.

Overview

Ozyde handles the complete rental lifecycle: browse, book, pay, receive, wear, return. The platform includes real-time availability tracking, personalised recommendations, multiple payment options, and a custom order service for made-to-measure dresses.

Tech Stack

Layer	Technology
Backend	PHP 7.4+
Database	MySQL 5.7+ (mysqli, PDO)
Frontend	HTML5, CSS3, Vanilla JavaScript
Authentication	Session-based, Google OAuth 2.0, 2FA
Email	PHPMailer (SMTP via Gmail)
APIs	Google Maps Places API, Google OAuth API
Libraries	Sortable.js, Font Awesome
Key Features

User Authentication

Secure registration with email verification
Google OAuth 2.0 login
Two-Factor Authentication (2FA) via email
Customer dashboard with profile and measurement management
Product Catalog

Dynamic filtering by category, size, colour, price range
Search across product names and descriptions
Two viewing modes: Shop (all products) and For You (personalised recommendations)
Wishlist with AJAX functionality
Load More pagination
Booking System

Interactive calendar with visual availability indicators
Three-day minimum rental period
Two-day cleaning buffer between bookings
Real-time availability checks
Variant-specific tracking (each size managed separately)
Checkout

Address autocomplete via Google Maps Places API
Multiple delivery and return options
Three payment methods: Card, Pay in Store (24-hour hold), EFT (2-hour verification)
Refundable deposit (R800)
Email confirmation via PHPMailer
Custom Orders

Custom dress design service with detailed form
Reference image uploads
Status tracking: pending, consultation, in progress, completed
Support

Help Centre with FAQ
Cleaning and Care Guide
Size Guide with metric, imperial, and international conversions
Contact form with WhatsApp integration
Database Structure

Table	Purpose
users	Account and profile data
products	Product catalogue
product_variants	Size-specific variants with individual pricing and stock
product_images	Multiple images per product
bookings	Confirmed rentals
cart	Temporary cart items
wishlist	Saved favourites
custom_orders	Custom dress requests
orders	Completed orders
categories	Product categorisation
dress_styles	Style preferences
user_measurements	Customer body measurements
messages	Contact form submissions
Security

Password hashing with bcrypt
Prepared statements for all database queries
CSRF protection with tokens
Input sanitisation and output escaping
2FA rate limiting (5 attempts max)
Session validation on all restricted pages
Getting Started

Requirements

PHP 7.4 or higher
MySQL 5.7 or higher
Composer
Installation

bash
git clone https://github.com/yourusername/ozyde.git
cd ozyde
composer install
Configuration

Update config.php with your database credentials:

php
define('DB_HOST', 'localhost');
define('DB_NAME', 'your_database');
define('DB_USER', 'your_username');
define('DB_PASS', 'your_password');
Set up Google OAuth credentials and Maps API keys in the respective configuration files.

File Structure

text
/ozyde/
├── index.php                 Landing page
├── catalog.php               Main catalogue (logged-in)
├── catalog_guest.php         Catalogue (guest)
├── productdetail.php         Product details
├── booking.php               Date selection
├── checkout.php              Checkout
├── cart.php                  Shopping cart
├── wishlist.php              Wishlist
├── customerdashboard.php     User dashboard
├── myrentals.php             Rental history
├── custom_orders.php         Custom order dashboard
├── register.php / login.php  Authentication
├── google_auth.php / callback.php  Google OAuth
├── admin/                    Admin panel
├── gallery/                  Product images
├── vendor/                   Composer dependencies
└── config.php                Configuration
License

This project is proprietary and confidential. Unauthorised copying, distribution, or use is strictly prohibited.

Contact

Ozyde Rentals
5 Liebenberg Rd, Noordwyk, Midrand 1687
Email: ozydedesigns@gmail.com
Instagram: @ozyde_
TikTok: @ozyde_designs
