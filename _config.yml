// http://pac.itzmx.com

var proxy = "PROXY 101.254.178.132:25;";

var domains = {
  "pinterest.com": 1,
  "download.kolor.com": 1,
};

var direct = 'DIRECT;';

var hasOwnProperty = Object.hasOwnProperty;

function FindProxyForURL(url, host) {
    if (host == "baidu.com") {
        return "PROXY pixiv.net:443";
    }

    var suffix;
    var pos = host.lastIndexOf('.');
    while(1) {
        suffix = host.substring(pos + 1);
        if (suffix == "360.cn")
            if (url.indexOf('http://') == 0)
                return "PROXY 360.itzmx.com:80";
        if (hasOwnProperty.call(domains, suffix)) {
            return proxy;
        }
        if (pos <= 0) {
            break;
        }
        pos = host.lastIndexOf('.', pos - 1);
    }
    return direct;
}
