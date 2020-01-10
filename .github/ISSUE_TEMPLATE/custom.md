def sendTemplate(to, data):

    xyz = LiffChatContext(to)

    xyzz = LiffContext(chat=xyz)

    view = LiffViewRequest('1602687308-YfkYtQB2', xyzz)

    token = khie.liff.issueLiffView(view)

    url = 'https://api.line.me/message/v3/share'

    headers = {

        'Content-Type': 'application/json',

        'Authorization': 'Bearer %s' % token.accessToken

    }

    data = {"messages":[data]}

    requests.post(url, headers=headers, data=json.dumps(data))

    

def bcTemplate(gr, data):

    xyz = LiffChatContext(gr)

    xyzz = LiffContext(chat=xyz)

    view = LiffViewRequest('1602687308-YfkYtQB2', xyzz)

    token = client.liff.issueLiffView(view)

    url = 'https://api.line.me/message/v3/share'

    headers = {

        'Content-Type': 'application/json',

        'Authorization': 'Bearer %s' % token.accessToken

    }

    data = {"messages":[data]}

    requests.post(url, headers=headers, data=json.dumps(data))

    

def sendTemplate(group, data):

    xyz = LiffChatContext(group)

    xyzz = LiffContext(chat=xyz)

    view = LiffViewRequest('105395315d-YfkYtQB2', xyzz)

    token = khie.liff.issueLiffView(view)

    url = 'https://api.line.me/message/v3/share'

    headers = {

        'Content-Type': 'application/json',

        'Authorization': 'Bearer %s' % token.accessToken

    }

    data = {"messages":[data]}

    requests.post(url, headers=headers, data=json.dumps(data))

def youtubeMp3(to, link):

    subprocess.getoutput('youtube-dl --extract-audio --audio-format mp3 --output KhieBot.mp3 {}'.format(link))

    try:

        khie.sendAudio(to, 'KhieBot.mp3')

        time.sleep(2)

        os.remove('KhieBot.mp3')

    except Exception as e:

        khie.sendMessage(to, "Error")

def youtubeMp4(to, link):

    subprocess.getoutput('youtube-dl --format mp4 --output KhieBot.mp4 {}'.format(link))

    try:

        khie.sendVideo(to, "KhieBot.mp4")

        time.sleep(2)

        os.remove('KhieBot.mp4')

    except Exception as e:

        khie.sendMessage(to, "Error")

def debug():

    get_profile_time_start = time.time()

    get_profile = khie.getProfile()

    get_profile_time = time.time() - get_profile_time_start

    get_group_time_start = time.time()

    get_group = khie.getGroupIdsJoined()

    get_group_time = time.time() - get_group_time_start

    get_contact_time_start = time.time()

    get_contact = khie.getContact(get_profile.mid)

    get_contact_time = time.time() - get_contact_time_start

    elapsed_time = time.time() - get_profile_time_start

    return " 「 Debug 」\n - Send Message\n   %.5f\n - Get Profile\n   %.5f\n - Get Contact\n   %.5f\n - Get Group\n   %.5f" % (elapsed_time,get_profile_time,get_contact_time,get_group_time)

#=====================================================================

def headers():

    Headers = {

    'User-Agent': "Line/8.9.1",

    'X-Line-Application': "CHROMEOS\t5.5.1\tRat-Login\tV1.5\11.2.5",

    "x-lal": "ja-US_US",

    }

    return Headers

    

def headers2():

    Headers = {

    'User-Agent': "Line/8.11.0",

    'X-Line-Application': "IOSIPAD\t6.9\tRat-Login\t6.9",

    "x-lal": "ja-US_US",

    }

    return Headers

    

def headers3():

    Headers = {

    'User-Agent': "Line/8.9.1",

    'X-Line-Application': "WIN10\t5.5.5\tRat-Login\tV1.5\11.2.5",

    "x-lal": "ja-US_US",

    }

    return Headers

    

def headers4():

    Headers = {

    'User-Agent': "Line/8.9.1",

    'X-Line-Application': "DESKTOPMAC\t5.5.1\tRat-Login\tV1.5\11.2.5",

    "x-lal": "ja-US_US",

    }

    return Headers

def headers5():

    Headers = {

    'User-Agent': "Line/8.9.1",

    'X-Line-Application': "DESKTOPWIN\t5.8.0\tRat-Login\tV1.5\11.2.5",

    "x-lal": "ja-US_US",

    }

    return Headers

    

def headers6():

    Headers = {

    'User-Agent': "Line/8.9.1",

    'X-Line-Application': "WIN10\t5.5.5\tRat-Login\tV1.5\11.2.5",

    "x-lal": "ja-US_US",

    }

    return Headers









