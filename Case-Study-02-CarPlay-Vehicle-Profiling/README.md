# Case Study 02: CarPlay Vehicle Profiling

## Scenario

After identifying the primary mobile device associated with the infotainment system during the device identification phase, I proceeded to determine who had access to the vehicle, how frequently they interacted with the CarPlay environment, and whether multiple individuals were using the same vehicle.

My objective was to establish a user profile of the vehicle by examining trusted pairings, historical CarPlay sessions, and user profile records stored within the Apple CarPlay ecosystem.

The analysis focused on three key artifacts:

- `carplay_pairing.dat`
- `carplay_sessions.dat`
- `device_users.dat`

These artifacts collectively revealed the identities of users, their devices, connection methods, application usage, and the frequency of vehicle interaction.

---

# Examination Details

| Item | Description |
|--------|-------------|
| Case ID | SANKOFA-CP-2025-0042 |
| Evidence Type | Apple CarPlay Logical Filesystem |
| Examination Tool | Autopsy 4.22.1 |
| Vehicle Profile | Sankofa Van 04 |
| Analysis Category | Vehicle Profiling |
| Examiner | Philip Oppong Adanse |

---

# Objective

The purpose of this examination was to:

- Identify all users associated with the vehicle.
- Determine trusted devices connected through Apple CarPlay.
- Establish ownership relationships between devices and drivers.
- Analyze vehicle usage patterns.
- Identify multiple-user activity within the infotainment ecosystem.

---

# Evidence Sources

## CarPlay Directory

```text
/private/var/mobile/Library/HIVE_CarPlay/
```

### Artifacts Examined

```text
carplay_pairing.dat
carplay_sessions.dat
device_users.dat
```

---

# Analysis 1: Trusted Device Pairings

The first artifact examined was:

```text
carplay_pairing.dat
```

This file contained records of devices that had been paired with the vehicle through Apple CarPlay.

The artifact provided information including:

- Vehicle name
- CarPlay identifier
- Driver name
- Device name
- Phone number
- Device model
- iOS version
- Bluetooth details
- Connection type
- Session counts
- Pairing history
- Trust status

---

## Evidence Screenshot

![CarPlay Pairings](images/01-carplay-pairings.png)

---

## Findings

### Daniel Owusu

I identified a trusted pairing belonging to Daniel Owusu.

| Attribute | Value |
|------------|---------|
| Driver | Daniel Owusu |
| Device | Daniel's iPhone |
| Phone Number | 0280104020 |
| Model | iPhone 14 |
| iOS Version | 16.5.1 |
| Vehicle | Sankofa Van 04 |
| Connection Type | Wireless |
| Total Sessions | 944 |
| Trusted | Yes |

This device recorded the highest number of vehicle interactions and appears to be the primary device associated with the vehicle.

---

### Kwame Mensah

A second trusted device was identified.

| Attribute | Value |
|------------|---------|
| Driver | Kwame Mensah |
| Device | Kwame's iPhone |
| Phone Number | 0287740012 |
| Model | iPhone 13 |
| iOS Version | 16.4 |
| Vehicle | Sankofa Van 04 |
| Connection Type | Wireless |
| Total Sessions | 587 |
| Trusted | Yes |

The session count indicates consistent interaction with the vehicle over time.

---

### Additional Pairing Records

I also identified evidence showing that Daniel Owusu's device had previously connected to:

```text
Toyota Corolla 2021
```

through a USB CarPlay connection.

This suggests that the device had been paired with multiple vehicles.

---

### Deleted Pairings

The artifact contained records of deleted pairings.

One deleted entry showed:

- Unknown user
- Unknown device
- Wireless connection
- Pairing deleted on 2025-04-19

The persistence of this record demonstrates that historical pairing information remained available even after removal from the infotainment system.

---

# Analysis 2: CarPlay Session Activity

The second artifact examined was:

```text
carplay_sessions.dat
```

This artifact recorded individual CarPlay sessions established between paired devices and the vehicle.

The records contained:

- Session start time
- Session end time
- Vehicle identifier
- Connection method
- Driver name
- Device information
- Session number
- Application activity

---

## Evidence Screenshot

![CarPlay Sessions](images/02-carplay-sessions.png)

---

# Findings

The session records revealed extensive historical activity involving multiple users.

---

## Daniel Owusu

The majority of recorded sessions were attributed to Daniel Owusu.

Applications frequently observed included:

- Apple Maps
- Google Maps
- Waze
- Spotify
- Messages
- Music

Repeated navigation application usage indicates regular travel activity while connected to the vehicle.

The large number of recorded sessions further supports Daniel's role as the primary vehicle operator.

---

## Kwame Mensah

Numerous sessions were attributed to Kwame Mensah.

Applications observed included:

- Apple Maps
- Google Maps
- Spotify
- Messages
- Waze

These records indicate routine access to the vehicle and consistent use of CarPlay services.

The volume of sessions suggests that Kwame was not an occasional passenger but an active vehicle user.

---

## Ama Owusu

The session logs also revealed activity associated with Ama Owusu.

Applications identified included:

- Apple Maps
- Google Maps
- Messages

Although the total number of sessions was lower than those associated with Daniel and Kwame, the records confirmed that Ama's device had successfully connected to the vehicle on multiple occasions.

---

# Analysis 3: User Profile Records

The final artifact examined was:

```text
device_users.dat
```

This file contained user profiles maintained within the CarPlay environment.

---

## Evidence Screenshot

![Device Users](images/03-device-users.png)

---

## Findings

Three user profiles were identified.

| User | Role |
|--------|--------|
| Daniel Owusu | Driver / Owner |
| Kwame Mensah | Relief Driver |
| Ama Owusu | Secondary User |

Associated profile identifiers included:

```text
CP-PROFILE-DANIEL
CP-PROFILE-KWAME
CP-PROFILE-AMA
```

The existence of multiple user profiles demonstrates that the infotainment system was configured for shared usage.

Each profile maintained its own identity within the vehicle environment.

---

# Correlation of Findings

By correlating all three artifacts, I established the following:

| User | Device | Phone Number | Vehicle Access |
|--------|---------|---------|---------|
| Daniel Owusu | Daniel's iPhone | 0280104020 | Primary User |
| Kwame Mensah | Kwame's iPhone | 0287740012 | Regular User |
| Ama Owusu | Ama's iPhone | 0285531188 | Secondary User |

The data consistently appeared across:

- Pairing records
- Session logs
- User profiles

This cross-artifact validation increases confidence in the findings.

---

# Interpretation

The evidence demonstrates that Sankofa Van 04 was not operated by a single individual.

Instead, the vehicle maintained a multi-user environment consisting of:

1. Daniel Owusu (Owner and Primary Driver)
2. Kwame Mensah (Relief Driver)
3. Ama Owusu (Secondary User)

The CarPlay ecosystem retained detailed records showing who connected, when they connected, and which applications were actively used during vehicle operation.

The high number of sessions associated with Daniel Owusu indicates that he was the principal operator of the vehicle.

---

# Conclusion

Through examination of `carplay_pairing.dat`, `carplay_sessions.dat`, and `device_users.dat`, I successfully reconstructed the user ecosystem associated with the vehicle.

The analysis identified three distinct users, multiple trusted devices, historical connection activity, and evidence of shared vehicle usage.

These findings establish the foundation for subsequent examinations involving route reconstruction, navigation analysis, communications correlation, and full incident timeline development.

---

## Key Findings

- Three unique CarPlay users identified.
- Multiple trusted devices connected to the vehicle.
- Daniel Owusu identified as the primary operator.
- Kwame Mensah identified as a regular relief driver.
- Ama Owusu identified as a secondary user.
- Historical pairing records preserved deleted device information.
- Session logs documented extensive navigation, communication, and media activity.
- Cross-artifact correlation confirmed a shared vehicle environment.
