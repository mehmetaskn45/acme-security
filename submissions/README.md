# 📤 Submission Guidelines

## 📋 Required Deliverables

### 1. Incident Report (PDF)

**Format:** PDF, max 5 pages  
**File name:** `FirstName_LastName_Report.pdf`

**Required Sections:**

#### Section 1: Incident Analysis (2-3 pages)
- Timeline reconstruction (UTC normalized)
- Attack vector identification
- Attack classification (MITRE ATT&CK, OWASP)
- Root cause analysis
- Impact assessment

#### Section 2: Architecture Review (1-2 pages)
- Current architecture weaknesses
- Improved security architecture diagram
- Recommended security controls (with justification)
- Defense-in-depth strategy

#### Section 3: Response & Remediation (1 page)
- Immediate actions (0-24 hours)
- Short-term fixes (1-2 weeks)
- Long-term improvements (1-3 months)
- Compliance considerations

**Formatting:**
- Professional appearance
- Clear structure with headers
- Evidence-based (reference logs)
- No excessive bullet points (use prose)

---

### 2. Video Presentation (MP4 or Link)

**Format:** MP4 or YouTube/Vimeo/Loom link  
**Duration:** 10-15 minutes  
**File name:** `FirstName_LastName_Video.mp4` or link in `video_link.md`

**Required Content:**

1. **Introduction (1 min)**
   - Brief self-introduction
   - Incident overview

2. **Attack Walkthrough (4-5 min)**
   - Show timeline
   - Explain attack techniques
   - Demonstrate with log examples
   - Root cause explanation

3. **Architecture Improvements (4-5 min)**
   - Present improved architecture
   - Explain design decisions
   - Walk through security layers

4. **Key Recommendations (2-3 min)**
   - Top 3 immediate actions
   - Long-term strategy summary

5. **Closing (1 min)**
   - Summary of key findings

**Video Guidelines:**
- ✅ Screen recording (no camera required, but welcome)
- ✅ Clear audio (use decent microphone)
- ✅ Readable slides/screen (1080p minimum)
- ✅ Professional background (if on camera)
- ❌ Do NOT upload large video files to GitHub (use links instead)

**Video Hosting:**
- Upload to YouTube (unlisted), Vimeo, or Loom
- Include link in `video_link.md` file

---

## 🚀 How to Submit via GitHub

### Prerequisites

Before starting, make sure you have:
- [ ] A GitHub account ([sign up here](https://github.com/signup) if needed)
- [ ] Git installed on your computer ([download here](https://git-scm.com/downloads))
- [ ] Your report PDF ready
- [ ] Your video uploaded and link ready

---

### Step-by-Step Submission Process

#### Step 1: Fork the Repository

**What is forking?** Creating your own copy of this repository.

1. Go to https://github.com/helloiamgp/acme-security
2. Click the **"Fork"** button in the top-right corner
3. Select your GitHub account as the destination
4. Wait a few seconds - you now have your own copy!

Your fork will be at: `https://github.com/YOUR_USERNAME/acme-security`

---

#### Step 2: Clone Your Fork to Your Computer

**What is cloning?** Downloading your fork to work on it locally.

Open your terminal (Mac/Linux) or Git Bash (Windows) and run:
```bash