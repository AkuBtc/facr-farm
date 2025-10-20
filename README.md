# facr-farm

# AgriInvest — Minimal Agricultural Investment Script

Overview
- PHP (PDO) + MySQL app for agricultural investments
- Frontend: register, login, KYC upload, invest
- Admin: manage users, view investments, review KYC
- Payment hooks: Stripe / PayPal / Paystack placeholders
- Built for shared hosting; no framework required

Requirements
- PHP 8.0+
- MySQL 5.7+
- mod_rewrite enabled (recommended)
- Writable storage/ and storage/kyc/ directories

Install
1. Create a MySQL database and user.
2. Import `install.sql` into your database.
3. Upload all files to your hosting account (public files to your site root).
4. Edit `app/config.php` with DB credentials and base URL.
5. Ensure storage/ and storage/kyc/ are writable by the web server (e.g., chmod 755/775 per host).
6. Configure payment gateway keys in `app/config.php`.
7. Zip for convenience (see below) or upload via FTP.

Quick zip command (Linux/macOS):
- From project root: `zip -r agriinvest.zip *`

Security & Notes
- Replace placeholder keys in config with real keys.
- Use SSL (HTTPS) in production.
- Set proper file permissions for uploaded KYC docs and protect storage from direct browsing.
- Integrate a production-grade KYC provider for real compliance.
- Test payments in sandbox mode first.

Support
Tell me which payment gateway you'd like active (Stripe, PayPal, Paystack, or others) and whether you want:
- Automatic payouts
- Referral/commission features
- Recurring investment/subscription plans

I'll then prepare a packaged zip or add gateway-specific implementation.

License
- MIT (feel free to modify)
