1. config.json
    disable_login_language_selector: forbidden user to change app language
    settingDefaults:
        showCommunitiesInsteadOfSpaces: which make the communities instead of space bar in left.Conbine with tagpanel.enableTagPanel and UIFeature.communities to hide the left bar.
        TagPanel.enableTagPanel: to hide the left bar combinde with showCommunitiesInsteadOfSpaces
        UIFeature.communities: false,
        language: which set the default language to zh-hans
        UIFeature.deactivate: which hide the user deactivate 
        UIFeature.passwordReset: which hide the password reset
        UIFeature.registration: which hide the registration
        UIFeature.feedback: which hide the timeline operate feedback
        MessageComposerInput.showStickersButton: which hide the sticker in input component
        UIFeature.shareQrCode: which hide the qrcode share
        UIFeature.flair: which hide the flair
        UIFeature.advancedSettings: which can hide the setting panel security tab advance settings include ignored users panel, invites panel, e2e panel
        breadcrumbs: which hide the shortcuts to recently viewed rooms above the room list
        piwik: which can hide the setting panel security tab privacy section and analytics, we set it empty
        UIFeature.conferenceEnabled: which set the voip visible in room
        ***************************yiqia add config**********************************************************
        EnableEncrypt: Which should hide all the encrypt function and ui features enclude cryptoEvent info, room security setting, app security setting, room avatar encurity show
                In here we thought that the encrypt is one features of the app and we the app should have the power to decide whether the app need the feature whenever the homeserver support is.
