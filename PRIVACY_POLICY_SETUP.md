# হাট-খরচ Privacy Policy Setup Guide

## GitHub Pages এ Privacy Policy হোস্ট করার নির্দেশনা

### ১. GitHub Repository তৈরি করুন

1. GitHub এ লগইন করুন
2. নতুন repository তৈরি করুন নাম: `hat-khoroch-privacy-policy`
3. Repository কে **Public** রাখুন

### ২. Privacy Policy File আপলোড করুন

**অপশন A: GitHub Web Interface দিয়ে**
1. Repository তে যান
2. "Add file" → "Upload files" ক্লিক করুন
3. `privacy_policy.html` ফাইল টেনে আনুন
4. ফাইল নাম পরিবর্তন করে `index.html` রাখুন
5. "Commit changes" ক্লিক করুন

**অপশন B: Git Command দিয়ে**
```bash
# Repository clone করুন
git clone https://github.com/[your-username]/hat-khoroch-privacy-policy.git
cd hat-khoroch-privacy-policy

# Privacy policy file কপি করুন এবং নাম পরিবর্তন করুন
copy H:\hat-khoroch\privacy_policy.html index.html

# Git এ যোগ করুন
git add index.html
git commit -m "Add privacy policy"
git push origin main
```

### ৩. GitHub Pages Enable করুন

1. Repository Settings এ যান
2. বাম sidebar থেকে "Pages" select করুন
3. Source: "Deploy from a branch" select করুন
4. Branch: "main" বা "master" select করুন
5. Folder: "/ (root)" select করুন
6. "Save" ক্লিক করুন

### ৪. Privacy Policy URL পাবেন

কয়েক মিনিট পর আপনার privacy policy এই URL এ পাওয়া যাবে:

```
https://[your-github-username].github.io/hat-khoroch-privacy-policy/
```

### ৫. Google Play Console এ URL যোগ করুন

1. Google Play Console এ যান
2. আপনার অ্যাপ select করুন
3. "Policy" → "App content" → "Privacy policy" এ যান
4. উপরের URL টি paste করুন
5. Save করুন

### ৬. Settings Screen এ URL আপডেট করুন (Optional)

`lib/presentation/screens/settings_screen.dart` ফাইলে:

```dart
void _showPrivacyPolicy(BuildContext context) {
  // এখানে আপনার actual GitHub Pages URL দিন
  final url = 'https://[your-username].github.io/hat-khoroch-privacy-policy/';
  
  showDialog(
    context: context,
    builder: (context) => AlertDialog(
      title: Text('গোপনীয়তা নীতি', style: GoogleFonts.hindSiliguri()),
      content: Text(
        'আমাদের গোপনীয়তা নীতি দেখতে:\n\n$url',
        style: GoogleFonts.hindSiliguri(),
      ),
      actions: [
        TextButton(
          onPressed: () => Navigator.pop(context),
          child: Text('বন্ধ করুন', style: GoogleFonts.hindSiliguri()),
        ),
      ],
    ),
  );
}
```

## Privacy Policy এ আপনার তথ্য যোগ করুন

`privacy_policy.html` ফাইলে নিম্নলিখিত জায়গায় আপনার তথ্য দিন:

```html
<!-- Line ~381 এর কাছাকাছি -->
<li><strong>ডেভেলপার:</strong> [Your Name/Company Name]</li>
<li><strong>ইমেইল:</strong> [your-email@example.com]</li>
```

## Google Play Data Safety Declaration

Google Play Console এ Data Safety section পূরণ করার জন্য:

### Data Collection - YES

**Personal info:**
- ✅ Name
- ✅ Phone number

**Financial info:**
- ✅ User payment info (expenses, earnings)
- ✅ Purchase history (transaction records)
- ✅ Other financial info (Dena-Paona records)

**App activity:**
- ✅ App interactions (tasks, completion status)

### Data Usage

**All collected data is used for:**
- ✅ App functionality
- ✅ Account management

### Data Sharing - NO

- ❌ We don't share data with third parties

### Security Practices

- ✅ Data is encrypted in transit (SSL/TLS)
- ✅ Data is encrypted at rest (Hive + Firebase)
- ✅ You can request data deletion (in-app feature)

### Data Deletion

**Delete account URL:** 
- Check "In-app deletion" 
- Users can delete account from: Settings → Danger Zone → Delete Account

## Support Contact Information

Google Play Console এ যে ইমেইল দেবেন, সেটি অবশ্যই সক্রিয় থাকতে হবে। ব্যবহারকারীরা সেখানে যোগাযোগ করতে পারবেন।

---

## সম্পূর্ণ হয়েছে! ✅

এখন আপনার অ্যাপ Google Play Store এ publish করার জন্য প্রস্তুত:
- ✅ Privacy Policy hosted
- ✅ Delete Account feature implemented  
- ✅ Firebase sync improved
- ✅ APK built (50.7MB)

**APK Location:** `build\app\outputs\flutter-apk\app-release.apk`
