# 🖼️ What is NFT Staking?

NFT staking is a smart contract mechanism that lets NFT holders **lock up their NFTs in exchange for rewards**, typically in the form of tokens.

Think of it like DeFi staking — but instead of tokens, you stake NFTs.

---

## 🎯 Why NFT Staking?

| Use Case          | Description                                        |
| ----------------- | -------------------------------------------------- |
| 🏆 Rewards        | Reward loyal holders with tokens (e.g. $XP, $VOTE) |
| 🎮 Game Mechanics | Lock NFTs to earn XP or boost in a game            |
| 📈 Reduce Supply  | Temporarily remove NFTs from circulation           |
| 💬 Governance     | Only staked NFTs allow voting or proposals         |

---

## ⚙️ How NFT Staking Works on Solana

Here’s how a typical NFT staking program is structured:

1. User sends their NFT to a PDA-controlled vault
2. A stake account is created to track:
   - owner pubkey
   - NFT mint
   - stake start timestamp
3. Rewards are calculated based on time staked
4. When user calls `claim` or `unstake`, tokens are distributed

---

## 🔐 Key Components

| Component          | Explanation                                   |
| ------------------ | --------------------------------------------- |
| Vault PDA          | Holds user NFTs while staked                  |
| Stake Account      | Stores stake state (owner, time, etc.)        |
| Reward Token       | SPL token given as reward                     |
| NFT Metadata Check | Ensure only certain collections are stakeable |

---

## 📦 Example Projects

| Project                | Highlights                                 |
| ---------------------- | ------------------------------------------ |
| MonkeDAO               | Staking SMB NFTs to earn DAO points        |
| Shadowy Super Coder    | Stake NFTs to earn $SHDW                   |
| Degenerate Ape Academy | Custom staking mechanics with rarity boost |
| Backpack/Frames        | Some NFTs unlock quests when staked        |

---

## 🧪 Tools & SDKs You Can Use

- **Metaplex** (for NFT metadata verification)
- **Anchor** (program logic)
- **Candy Guard** (if minting + staking hybrid)
- **Bubblegum** (for compressed NFTs)

---

## 🧠 Want to Build One?

You can build a simple NFT staking dApp that:

- Verifies NFT belongs to a specific verified collection
- Locks the NFT in a PDA
- Tracks how long it's staked
- Mints SPL tokens as reward on claim

> I can scaffold that in Anchor + React if you’d like 🚀

---

## 🚨 Security Tips

- Always validate `metadata.creator` to ensure NFTs are legit
- Use `anchor-lang` to safely deserialize accounts
- Lock staking/unstaking to **signed users only**
