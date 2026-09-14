# smart-rehab-sleeve
Wearable sleeve that tracks joint movement in real time to guide home physiotherapy exercises
# Smart Rehabilitation Sleeve 🦾

**Real-time motion feedback for home physiotherapy — so recovery doesn't stop when the therapist leaves the room.**

Submission for the **SmartX Hackathon 2026** — Healthcare Track
Organized by ITIDA – EME Innovation Labs, Creativa Giza

---

## The Problem

Most physiotherapy plans include exercises patients must repeat at home between clinic sessions. But:

- A physiotherapist can't be present for every repetition — sessions happen once or twice a week at best.
- Without supervision, patients often use the wrong range of motion, the wrong pace, or simply skip sessions.
- This slows recovery and risks re-injury, especially for post-surgery, stroke, and orthopedic patients.

**No physiotherapist. No feedback. No way to know if it's working.**

## Our Solution

A wearable sleeve embedded with motion sensors that tracks every repetition of a prescribed exercise, gives the patient instant feedback on form, and reports adherence data to their physiotherapist remotely.

| | |
|---|---|
| **Tracks** | IMU + flex sensors sewn into the sleeve measure joint angle and movement speed in real time, on the knee, elbow, or wrist. |
| **Guides** | Instant feedback — light, sound, or app cue — tells the patient if a rep matches the range and pace the therapist prescribed. |
| **Reports** | Every session syncs to a dashboard the physiotherapist can review remotely, without the patient traveling in. |

## How It Works — Example: Knee Rehabilitation

The patient performs a prescribed **bend → straighten → bend → straighten** cycle. The sleeve measures joint angle continuously through the cycle, counting reps, checking range of motion, and flagging incomplete or rushed movements.

Example session output:
- **Reps completed:** 14 / 15
- **Range of motion:** 92% of target
- **Form flag:** 1 rushed rep

## Tech Stack (MVP)

**Hardware**
- IMU sensor (e.g. MPU6050) — captures joint angle and rotational movement
- Flex sensor strip — confirms bend direction and adds redundancy to angle readings
- Microcontroller (ESP32) — runs on-device rep counting and streams data over Bluetooth
- Rechargeable battery — keeps the sleeve wireless and wearable through a full session

**Software**
- Companion mobile app — guides the patient through the prescribed exercise, live
- Real-time feedback engine — turns angle + speed data into an instant correct/incorrect cue
- Therapist dashboard — session history, adherence trend, and flagged reps for remote review
- Cloud sync — session data pushed after each use for the therapist to check anytime

## Why It Matters

- **Aging & chronic care demand** — post-surgery, stroke, and orthopedic patients increasingly rely on home exercise programs as clinics stay overbooked.
- **Better recovery outcomes** — objective feedback on form and range of motion helps patients recover correctly, not just "eventually."
- **Extends the physiotherapist** — one therapist can safely oversee more patients remotely when the sleeve reports adherence and flags problems.

## Grounded in Research

IMU and flex-sensor wearables for tracking joint range of motion are an established research area — published designs have measured finger and limb joint angle within a few percent of a clinical goniometer. We're building on validated sensing, not unproven hardware.

**Where we differentiate:** most prior work stops at measurement. We close the loop — real-time patient feedback during the exercise itself, plus a remote therapist dashboard — built for a market where physiotherapist access is limited outside major cities.

## Demo Plan

1. **Live wear-test** — a teammate wears the sleeve and performs a knee bend/straighten cycle on stage.
2. **Real-time app view** — the companion app shows live angle tracking, rep count, and instant correct/incorrect feedback.
3. **Therapist dashboard** — session log with adherence, range of motion trend, and flagged reps, as a therapist would see it.
4. **The pitch close** — tying back to the access gap this solves.

## Status

🚧 Early-stage — application phase for SmartX Hackathon 2026. Hardware prototyping and app development in progress ahead of the final round.

## Team

*(add your team members' names and roles here)*

## License

*(add a license if you plan to open-source this, e.g. MIT — optional for a hackathon repo)*
