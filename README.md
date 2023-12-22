# Game Circle SDK
A wrapper SDK for Unity that connects the most used SDKs in a modular fashion.


1) Go to **File → Build Settings** and make sure **Platform** is set to **Android** or **iOS**.
2) Go to **File → Build Settings** window, make sure that every scene your game will use is included under the **Scenes in Build** section.
3) Go to **File → Build Settings → Player Settings** and do the following:
   * On top, set **Company Name** and **Product Name**.
   * Under the **Icon → Adaptive** tab set both **Background** and **Foreground** to your icon.
   * Under the **Other Settings** tab set the following:
     * **Target API Level** = API Level 34
     * **Scripting Backend** = IL2CPP
     * **ARM64** = checked
   * Under the **Publishing Settings** tab, check **Custom Keystore**, and make sure your keystore file is selected correctly.
4) In the project folders, open the file **Assets → Plugins → Android → AndroidManifest.xml**, and make sure the variable **android:debuggable** is set to **false**.
5) Download GameCircleSDK-v.x.y.z.unitypackage and import it to your project by selecting the file under **Assets → Import Package → Custom Package**.
6) If at any point after this step, the **Enable Android Auto-resolution?** window pops up, click **Enable**, and wait for the resolver to finish before continuing with the next step.
7) After Unity is done importing the files, open the first scene in the project (the scene with index 0 under **File → Build Settings → Scenes in Build**), and drag **Assets/GameCircleSDK/Prefabs/GameCircleSDK.prefab** file into your hierarchy. This Game Object can be situated anywhere in the hierarchy as long as its parent is the scene itself, i.e. it is not a child of another Game Object in the scene.
8) Click **Game Circle → Settings**, and the settings panel will appear in the Inspector view.
   * If you were given any, paste you **Data ID** in the corresponding input field and click **Fetch**. This will automatically fetch all the settings and IDs for you.
   * If you are configuring your SDKs by hand, mark the ones you want to use and input the IDs.
9) If you are using the Facebook SDK, go to **File → Build Settings → Player Settings → Publishing Settings**, copy the **Custom Keystore Path** (example: C:/Users/…/xyz.keystore) and paste it to **Android Keystore Path** section in **Game Circle → Settings**.
