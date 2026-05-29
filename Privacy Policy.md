# 🛡️ Privacy Policy for Fira

Welcome to the **Fira** Privacy Policy. We value your privacy and believe in full transparency regarding how your data is handled. By inviting Fira to your Discord server or utilizing its features, you consent to the data practices described below.

> [!NOTE]  
> **Quick Summary:** Fira only collects data necessary for its features to work properly. **We do not sell, rent, or share your data with third parties.** 

---

## 🗄️ Data Flow & Storage (Visualized)

To help you understand exactly where your data goes, here is a visual representation of Fira's data lifecycle:

```mermaid
flowchart TD
    User(["Discord User / Admin"]) -->|"Inputs Commands & Profiles"| Bot{"Fira Bot"}
    
    Bot -->|"Stores Data Locally"| DB[("Local Secure Database")]
    DB -.->|"Loads Settings on Command"| Bot
    
    Bot -->|"Optional Integration"| LastFM["Last.fm API"]
    Bot -.->|"❌ STRICTLY PROHIBITED"| ThirdParties["Advertisers / Data Brokers"]
    
    style User fill:#5865F2,stroke:#fff,stroke-width:2px,color:#fff
    style Bot fill:#EB459E,stroke:#fff,stroke-width:2px,color:#fff
    style DB fill:#FEE75C,stroke:#000,stroke-width:2px,color:#000
    style ThirdParties fill:#ED4245,stroke:#fff,stroke-width:2px,color:#fff
```

> [!IMPORTANT]  
> As shown above, your data **never** leaves the bot's ecosystem unless you are explicitly using an integration like Last.fm. 

---

## 📊 1. Data We Collect & Store

To provide you with the best music and bot experience, Fira uses a secure local database. Here is exactly what we store:

### 👤 User Information
| Type of Data | What it is | Why we need it |
| --- | --- | --- |
| **Discord IDs** | Your unique Discord identifier. | To link your profile, settings, and permissions to you. |
| **Social Profiles** | Badges, bio, friends list, and marriage status. | To display your custom bot profile using our commands. |
| **Settings** | Music platform preference (e.g., YouTube Music). | To tailor your music searching experience. |
| **Last.fm Data** | Username, avatar, display name, and play counts. | To fetch and display your listening stats via the Last.fm integration. |

### 🏘️ Server (Guild) Information
| Type of Data | What it is | Why we need it |
| --- | --- | --- |
| **Discord IDs** | The unique ID of the server. | To store configuration specifically for your community. |
| **Configurations** | Custom prefixes, voice roles, ignored channels. | To allow server admins to customize how the bot operates. |
| **Setup Data** | Channel IDs and Message IDs for 24/7 or Music Request panels. | To keep automation and music request features active and functioning. |

### 🎵 Music & Playlists
| Type of Data | What it is | Why we need it |
| --- | --- | --- |
| **Custom Playlists** | Playlist names, saved track URIs, durations, and titles. | To allow you to save and instantly load your favorite songs. |
| **Permissions** | User IDs of members you invite to edit your playlists. | To allow collaborative playlist management. |

### 🛑 Moderation & Security
| Type of Data | What it is | Why we need it |
| --- | --- | --- |
| **Blacklists** | User or Server IDs that are banned from using the bot. | To protect the bot from abuse. |
| **Access Control** | No-prefix access data and specific rank permissions. | To grant premium or administrative access to authorized users. |

---

## ⚙️ 2. How Your Data is Used

> [!TIP]  
> **Your data stays with Fira.** We strictly use your data to power the bot's functionality. 

- **Executing Commands:** Remembering your setup configurations so you don't have to input them every time.
- **Automation:** Assigning voice roles or automatically connecting to 24/7 voice channels based on your saved server settings.
- **Integrations:** Only communicating with verified third-party APIs (like Last.fm or Lavalink) directly related to commands you intentionally trigger.

---

## ⏳ 3. Data Retention Lifecycle

Data is kept in Fira's database as long as it remains relevant to the bot's operations. Here is how we treat different types of data over time:

```mermaid
flowchart LR
    Data["User / Server Data"] --> Type{"Data Type"}
    
    Type -->|"Profiles & Playlists"| Perm["Retained Indefinitely"]
    Type -->|"Temp Blacklists / Access"| Temp["Has Expiration Date"]
    Type -->|"Server Configs"| Dormant["Kept Dormant if Bot Kicked"]
    
    Temp -->|"Timer Reaches 0"| AutoDelete(("Auto-Deleted by Bot"))
    Perm -->|"User Requests Wipe"| Wipe(("Permanently Wiped"))
    
    style Data fill:#5865F2,stroke:#fff,color:#fff
    style AutoDelete fill:#10B981,stroke:#fff,color:#fff
    style Wipe fill:#EF4444,stroke:#fff,color:#fff
```

- **Active Data:** Profiles, settings, and playlists are retained indefinitely while you use the bot.
- **Temporary Data:** Time-limited no-prefix access or blacklists are automatically invalidated upon expiration.
- **Orphaned Data:** If Fira is removed from a server, server-specific configurations remain dormant. 

---

## 🗑️ 4. Your Rights (Data Deletion Process)

You have full control over your digital footprint. If you wish to have your data erased, the process is straightforward:

```mermaid
flowchart TD
    Start(["You Want Data Deleted"]) --> Step1["Leave Support Server & Kick Bot"]
    Step1 --> Step2["Contact Developer Team"]
    
    Step2 --> Action{"Developer Action"}
    Action -->|"Verifies ID"| Delete["Runs Database Wipe Command"]
    
    Delete --> End(("Data Permanently Erased"))
    
    style Start fill:#F59E0B,stroke:#fff,color:#fff
    style End fill:#EF4444,stroke:#fff,color:#fff
```

1. **Server Data:** Server administrators can remove the bot, and manually clear channel configurations by deleting the associated channels.
2. **Personal Data Wipes:** If you want your user profile, Last.fm connections, and custom playlists entirely wiped from our systems, please contact the developer team to execute the wipe.

> [!WARNING]  
> Once a developer manually deletes your profile data upon request, it is **permanently lost** and cannot be recovered.

---

## 📬 5. Contact & Support

If you have any questions about this Privacy Policy, your stored data, or if you'd like to submit a data deletion request, please reach out to the bot developers through our support channels.

*Last Updated: May 2026*
