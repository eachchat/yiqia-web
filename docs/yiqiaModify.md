1. config.json
    disable_login_language_selector: forbidden user to change app language
    settingDefaults:
        showCommunitiesInsteadOfSpaces: which make the communities bar in left hidden.
        language: which set the default language to zh-hans
        UIFeature.deactivate: which hide the user deactivate 
        UIFeature.passwordReset: which hide the password reset
        UIFeature.registration: which hide the registration
        UIFeature.feedback: which hide the timeline operate feedback
        MessageComposerInput.showStickersButton: which hide the sticker in input component
        UIFeature.shareQrCode: which hide the qrcode share
        UIFeature.flair: which hide the flair
        breadcrumbs: which hide the shortcuts to recently viewed rooms above the room list
        ***************************yiqia add config**********************************************************
        EnableEncrypt: Which should hide all the encrypt function and ui features enclude cryptoEvent info, room security setting, app security setting, room avatar encurity show
                In here we thought that the encrypt is one features of the app and we the app should have the power to decide whether the app need the feature whenever the homeserver support is.
