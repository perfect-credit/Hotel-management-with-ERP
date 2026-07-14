# Havenir Hotel ERPNext

Havenir Hotel ERPNext is an ERPNext/Frappe application that adds hotel and restaurant management features to an ERPNext site. It provides doctypes and UI for check-ins, check-outs, room management, food orders, laundry, payments and related workflows.

**Key features**
- Hotel check-in and check-out flows with room assignment and occupancy tracking
- Room types, facilities and room management
- Food ordering and restaurant table support
- Laundry order management
- Checkout payments, taxes and charges handling
- Guest records and basic reporting hooks

**Repository layout**
- `havenir_hotel_erpnext/` — Frappe app package and metadata
- `havenir_hotel_erpnext/havenir_hotel_erpnext/doctype/` — DocType implementations (check-in, check-out, rooms, food orders, guests, laundry, payments, etc.)
- `fixtures/custom_field.json` — example fixtures for custom fields

**Installation (typical)**
1. Ensure you have a working Frappe/ERPNext bench environment.
2. In your bench's `apps` folder, clone or install this app:

```bash
cd ~/frappe-bench/apps
git clone <this-repo-url> havenir_hotel_erpnext
cd ~/frappe-bench
bench --site your-site install-app havenir_hotel_erpnext
bench restart
```

3. Import fixtures if needed (from `fixtures/custom_field.json`) via `bench --site your-site import-fixtures` or the UI.

**Running tests**
- To run the app tests with bench:

```bash
bench run-tests --app havenir_hotel_erpnext
```

**Development**
- DocTypes live under `havenir_hotel_erpnext/havenir_hotel_erpnext/doctype/`.
- Frontend JS for list and form views are next to their DocType definitions (`*.js`).
- When developing, use `bench start` (or `bench watch`) and reload the site to see changes.

**Contributing**
- Please open issues for bugs or feature requests.
- For code contributions, fork the repository, create a feature branch and open a pull request.

**License**
- MIT

**Contact / Support**
- For questions or support, open an issue in this repository.
