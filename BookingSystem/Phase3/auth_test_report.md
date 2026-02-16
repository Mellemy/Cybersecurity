
### 🧑‍🦲 **Guest**

---

**✅ Can do**

List every action a *Guest* can perform, with the page or endpoint.
Example format:

* “Can access login form — `/login`”
* “Can access registration form — `/register`”
* “Can view registered reservations without identity — `/` (spec 8)”
* “Can see the username, email, and user token of all accounts. — `/api/users` (critical. ⚠️)”
* “Can access resource name and descriptions — `/api/resources` (These arent supposed to be visible to guests.⚠️)”
* “Can create a new resource — `/resources`”  (Broken access control. Users can use /resources directly without the button. ⚠️)
* “Can access reservations — `/api/reservations`”  (The user can see ID's but is unauthorized from using them maliciously.)


---

**❌ Cannot do**

List every action that a *Guest* is blocked from doing.
Example format:

* “Cannot edit other users reservations``/reservation/id`”
* “Cannot edit a resource — ``/resources/id`"
* “Cannot view users of reservations  — `/`”
* “Cannot book a resource — ``/reservation`”

---

### 🧑‍💼 **Reserver**

---

**✅ Can do**

List actions a *Reserver* can do according to specs + actual test results.
Include visible pages **and** API endpoints.

Example format:

* “Can book a resource — ``/reservation`”
* “Can create a new resource — `/resources`” (Not supposed to? )
* “Can view reservations — `/` (spec 8)”
* “Can logout  — `/logout`”
* “Can delete own reservations”
* “Can edit own reservation — ``/reservation/id`” (includes changing time, resource reserved. )
* “Can change user of own reservation — ``/reservation/id`” (This is NOT how its supposed to work! Flaw in business logic ⚠️)
* “Can see the username, email, and user token of all accounts. — `/api/users` (critical ⚠️)”
* “Can access resource name and descriptions — `/api/resources` (Reservers shouldnt be able to see resource descriptions.⚠️) ”
* “Can access reservations — `/api/reservations`” 

**❌ Cannot do**

List actions a *Reserver* is correctly blocked from.

Example format:
* “Cannot edit other users reservations``/reservation/id`”
* “Cannot edit a resource — ``/resources/id`"


---

### 🧑‍💼🛡️ **Administrator**

---

**✅ Can do**

List actions an *Administrator* can perform.

Example format:

* “Can book a resource — ``/reservation`”
* “Can create a new resource — `/resources`”
* “Can view registered reservations — `/` (spec 8)”
* “Can logout  — `/logout`”
* “Can delete existing reservations.”
* “Can edit a reservation — ``/reservation/id`” (includes changing time, resource reserved, and user reserving it.)"
* “Can change user of any reservation — ``/reservation/id`” (Business logic flaw (I think) ⚠️)
* “Can edit a resource — ``/resources/id`” (includes changing resource name and description)"
* “Can see the username, email, and user token of all accounts. — `/api/users` (critical ⚠️)”
* “Can access resource name and descriptions — `/api/resources` (no harm?)
* “Can access reservations — `/api/reservations`” 
---

**❌ Cannot do**

List prohibited behaviors, if any, or incorrect implementation issues.

Example format:

* “Cannot delete existing resources — ``/resources/id`”" (A resource cant be deleted. Should be fixed ⚠️)
---
