# WinRAR-Keygen-Web
WinRAR Keygen Web for Code Javascript

xin lưu ý:
các thuật toán tạo khóa của winrar không hổ trợ định dạng văn bản utf-8
nên khi bạn cố gắng tạo:
username và licensetype bằng văn bản có các ký tự đặc biệt.
phần mềm winrar sẽ báo lỗi license không hợp lệ.


#tổng hợp 1 số tool tạo keygen winrar online sử dụng công nghệ wasm
https://winrar.netlify.app/

chia sẽ một số thông tin thêm về định hướng cho các dự án phát triển tư duy công nghệ tiên tiến "ALL IN ONE"

# 🚀 WinRAR Premium

**WinRAR Premium** là công cụ hỗ trợ tải, cài đặt, cập nhật và tự động kích hoạt bản quyền WinRAR một cách dễ dàng. Dựa trên API cập nhật chính thức, phần mềm này giúp người dùng luôn sử dụng phiên bản WinRAR mới nhất với `rarreg.key` được tạo tự động và đầy đủ thông tin đăng ký.

---

## 📦 Tính năng chính

- ✅ **Sử dụng API chính thức từ 721PC:**
  - `https://api.itdev721.workers.dev/?action=WinrarVersionJson`
  - Lấy dữ liệu về phiên bản (`VersionBeta`) và số hiệu bản dựng (`NumberversionCurrent`)

- 🔍 **Phát hiện phiên bản WinRAR trên máy:**
  - Kiểm tra hệ thống xem WinRAR đã được cài đặt chưa
  - Nếu chưa cài đặt: hiển thị chức năng tải và cài đặt
  - Nếu đã cài đặt: so sánh phiên bản hiện tại với phiên bản mới nhất từ API

- ⚙️ **Tự động cập nhật WinRAR:**
  - Khi phát hiện phiên bản mới → hiển thị nút cập nhật
  - Tải bản cập nhật và cài đè vào phiên bản cũ

- 🔑 **Tạo file `rarreg.key` tự động:**
  - Nhập thông tin đăng ký (tên người dùng, công ty, email,...) vào form
  - Tạo `rarreg.key` theo chuẩn WinRAR và đặt vào thư mục gốc của cài đặt

- 🖥️ **Tùy chọn cài đặt linh hoạt:**
  - Lựa chọn phiên bản WinRAR
  - Lựa chọn ngôn ngữ
  - Lựa chọn hệ điều hành 32-bit hoặc 64-bit

- 🔄 **Tự động kiểm tra cập nhật mỗi khi khởi động máy:**
  - Thông qua Windows Service chạy ngầm

  -**MÃ NGUỒN GỐC TẠO KEYGEN BẰNG JAVASCRIPT**
<pre style="max-height: 300px; overflow-y: auto; background-color: #f4f4f4; padding: 10px;">
<code>

const GF2_15_exp_tab = generateGF2_15_exp_tab();
const GF2_15_log_tab = generateGF2_15_log_tab();

function generateGF2_15_exp_tab() {
    const EXP_SIZE = 0x7fff; // 32767
    const exp_tab = new Uint32Array(EXP_SIZE);
    let p = 1;
    exp_tab[0] = 1;

    for (let i = 1; i < EXP_SIZE; i++) {
        p <<= 1;
        if (p > EXP_SIZE) {
            p ^= 0x8003; // Polynomial x^15 + x + 1
        }
        exp_tab[i] = p;
    }
    return exp_tab;
}

function generateGF2_15_log_tab() {
    const EXP_SIZE = 0x7fff; // 32767
    const LOG_SIZE = 0x7fff + 1; // 32768
    const log_tab = new Uint32Array(LOG_SIZE);
    log_tab[1] = 0;

    for (let i = 0; i < EXP_SIZE; i++) {
        log_tab[GF2_15_exp_tab[i]] = i;
    }
    log_tab[0] = 0; // Special case

    return log_tab;
}

function CRC32(r) { for (var a, o = [], c = 0; c < 256; c++) { a = c; for (var f = 0; f < 8; f++)a = 1 & a ? 3988292384 ^ a >>> 1 : a >>> 1; o[c] = a } for (var n = -1, t = 0; t < r.length; t++)n = n >>> 8 ^ o[255 & (n ^ r.charCodeAt(t))]; return (n) >>> 0 };

function Bytes_to_BigInt(b) {
    var ans = 0n;
    for (var i = 0; i < b.length; i++) {
        ans = ans + (BigInt(((b[i]).charCodeAt(0)) & 0x0ff) << (BigInt(i * 8)));
    }
    return ans;
}
function BigInt_to_Bytes(b, l) {
    var ans = "";
    var _b = 0n;
    var c = 0;
    _b = BigInt(b);
    for (var k = 0; k < l; k++) {
        c = Number(_b % (BigInt(256))) & 0x0ff;
        ans = (String.fromCharCode(c)) + ans;
        _b = (_b >> (8n));
    }
    return ans;
}
function Bytes_to_Hex(b) {
    var ans = "";
    for (var i = 0; i < b.length; i++) {
        ans = ans + (((((b[i]).charCodeAt(0)) & 0x0ff).toString(16)).padStart(2, '0'));
    }
    return ans;
}
function GF_add(a, b) {
    return (a ^ b);
}

function GF_sub(a, b) {
    return (a ^ b);
}

function GF_mul(a, b) {

    function GF215_mul(s1, s2) {
        if ((s1 == 0) || (s2 == 0)) { return 0; }
        else { return (GF2_15_exp_tab[(GF2_15_log_tab[s1] + GF2_15_log_tab[s2]) % (0x07fff)]); }
    }

    if ((a == 0n) || (b == 0n)) { return 0n; }
    else {
        var Ta = new Uint32Array(17);
        var Tb = new Uint32Array(17);
        var Tc = new Uint32Array(34);
        var k, r, res;
        for (k = 0; k < 17; k++) {
            Ta[k] = Number(a & (0x07fffn));
            Tb[k] = Number(b & (0x07fffn));
            a = a >> (15n);
            b = b >> (15n);
        }

        for (k = 0; k < 34; k++) { Tc[k] = 0; }
        for (k = 0; k < 17; k++) { for (r = 0; r < 17; r++) { Tc[k + r] ^= GF215_mul(Ta[k], Tb[r]); } }
        for (k = 33; k > 16; k--) {
            Tc[k - 17] ^= Tc[k];
            Tc[k - 14] ^= Tc[k];
            Tc[k] = 0;
        }
        res = 0n;
        for (k = 16; k > 0; k--) { res = ((res + BigInt(Tc[k])) << (15n)); }
        res = (res + BigInt(Tc[0]));
        return res;
    }
}

function GF_inv(a) {
    if (a == 0n) { return 0n; }
    else {
        var base, ans, temp, r;
        base = a;
        ans = 1n;
        temp = 0n;
        for (r = 0; r < 16; r++) {
            base = GF_mul(base, base);
            base = GF_mul(base, base);
            base = GF_mul(base, base);
            base = GF_mul(base, base);
            base = GF_mul(base, base);
            base = GF_mul(base, base);
            base = GF_mul(base, base);
            base = GF_mul(base, base);
            base = GF_mul(base, base);
            base = GF_mul(base, base);
            base = GF_mul(base, base);
            base = GF_mul(base, base);
            base = GF_mul(base, base);
            base = GF_mul(base, base);
            base = GF_mul(base, base);
            ans = GF_mul(ans, base);
        }
        temp = GF_mul(ans, a);
        temp = BigInt(GF2_15_exp_tab[(0x07fff - GF2_15_log_tab[Number(temp & (0x07fffn))]) % (0x07fff)]);
        ans = GF_mul(ans, temp);
        return ans;
    }
}

function GF_div(a, b) { return GF_mul(a, GF_inv(b)); }

function ECP_double(a) {
    if (a == 0n) { return a; }
    else {
        var _x, _y, m;
        var newx, newy;
        _x = a & (0x07fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffn);
        _y = (a >> (255n)) & (0x07fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffn);
        m = GF_add(GF_div(_y, _x), _x);
        newx = (GF_add(GF_mul(m, m), m));
        newy = (GF_add(GF_mul(GF_add(m, 1n), newx), GF_mul(_x, _x)));
        return (newx | (newy << (255n)));
    }
}
function ECP_add(a, b) {
    var a_x, a_y, b_x, b_y, m;
    var newx, newy;
    a_x = a & (0x07fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffn);
    a_y = (a >> (255n)) & (0x07fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffn);
    b_x = b & (0x07fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffn);
    b_y = (b >> (255n)) & (0x07fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffn);
    if (a == b) {
        return ECP_double(a);
    }
    else if ((a_x == 0n) && (a_y == 0n)) {
        return b;
    }
    else if ((b_x == 0n) && (b_y == 0n)) {
        return a;
    }
    else if ((a_x == 0n) && (b_x == 0n) && (a_y != 0n) && (b_y != 0n)) {
        return 0n;
    }
    else {
        m = GF_div(GF_add(a_y, b_y), GF_add(a_x, b_x));
        newx = (GF_add(GF_add(m, GF_mul(m, m)), GF_add(a_x, b_x)));
        newy = (GF_add(GF_mul(m, GF_add(a_x, newx)), GF_add(newx, a_y)));
        return (newx | (newy << (255n)));
    }
}

function ECP_smul(k, a) {
    if (k == 0n) { return 0n; }
    else {
        var _k, _a, ans;
        _k = k % (0x01026dd85081b82314691ced9bbec30547840e4bf72d8b5e0d258442bbcd31n);
        _a = a;
        ans = 0n;
        while (_k != 0n) {
            if ((_k & (1n)) != 0n) {
                ans = ECP_add(ans, _a);
            }
            _a = ECP_add(_a, _a);
            _k = (_k >> (1n));
        }
        return ans;
    }
}

function SHA1(msg) {
    function rotate_left(n, s) {
        return ((n << s) | (n >>> (32 - s)));
    };
    function cvt_hex(val) {
        var str = '';
        str += ((val >>> 28) & 0x0f).toString(16);
        str += ((val >>> 24) & 0x0f).toString(16);
        str += ((val >>> 20) & 0x0f).toString(16);
        str += ((val >>> 16) & 0x0f).toString(16);
        str += ((val >>> 12) & 0x0f).toString(16);
        str += ((val >>> 8) & 0x0f).toString(16);
        str += ((val >>> 4) & 0x0f).toString(16);
        str += (val & 0x0f).toString(16);
        return str;
    };
    var blockstart;
    var i, j;
    var W = new Array(80);
    var H0 = 0x067452301;
    var H1 = 0x0EFCDAB89;
    var H2 = 0x098BADCFE;
    var H3 = 0x010325476;
    var H4 = 0x0C3D2E1F0;
    var A, B, C, D, E;
    var temp;
    var msg_len = msg.length;
    var word_array = new Array();
    for (i = 0; i < msg_len - 3; i += 4) {
        j = msg.charCodeAt(i) << 24 | msg.charCodeAt(i + 1) << 16 | msg.charCodeAt(i + 2) << 8 | msg.charCodeAt(i + 3);
        word_array.push(j);
    }
    switch (msg_len % 4) {
        case 0:
            i = 0x080000000;
            break;
        case 1:
            i = msg.charCodeAt(msg_len - 1) << 24 | 0x0800000;
            break;
        case 2:
            i = msg.charCodeAt(msg_len - 2) << 24 | msg.charCodeAt(msg_len - 1) << 16 | 0x08000;
            break;
        case 3:
            i = msg.charCodeAt(msg_len - 3) << 24 | msg.charCodeAt(msg_len - 2) << 16 | msg.charCodeAt(msg_len - 1) << 8 | 0x080;
            break;
    }
    word_array.push(i);
    while ((word_array.length % 16) != 14) word_array.push(0);
    word_array.push(msg_len >>> 29);
    word_array.push((msg_len << 3) & 0x0ffffffff);
    for (blockstart = 0; blockstart < word_array.length; blockstart += 16) {
        for (i = 0; i < 16; i++) W[i] = word_array[blockstart + i];
        for (i = 16; i <= 79; i++) W[i] = rotate_left(W[i - 3] ^ W[i - 8] ^ W[i - 14] ^ W[i - 16], 1);
        A = H0;
        B = H1;
        C = H2;
        D = H3;
        E = H4;
        for (i = 0; i <= 19; i++) {
            temp = (rotate_left(A, 5) + ((B & C) | (~B & D)) + E + W[i] + 0x05A827999) & 0x0ffffffff;
            E = D;
            D = C;
            C = rotate_left(B, 30);
            B = A;
            A = temp;
        }
        for (i = 20; i <= 39; i++) {
            temp = (rotate_left(A, 5) + (B ^ C ^ D) + E + W[i] + 0x06ED9EBA1) & 0x0ffffffff;
            E = D;
            D = C;
            C = rotate_left(B, 30);
            B = A;
            A = temp;
        }
        for (i = 40; i <= 59; i++) {
            temp = (rotate_left(A, 5) + ((B & C) | (B & D) | (C & D)) + E + W[i] + 0x08F1BBCDC) & 0x0ffffffff;
            E = D;
            D = C;
            C = rotate_left(B, 30);
            B = A;
            A = temp;
        }
        for (i = 60; i <= 79; i++) {
            temp = (rotate_left(A, 5) + (B ^ C ^ D) + E + W[i] + 0x0CA62C1D6) & 0x0ffffffff;
            E = D;
            D = C;
            C = rotate_left(B, 30);
            B = A;
            A = temp;
        }
        H0 = (H0 + A) & 0x0ffffffff;
        H1 = (H1 + B) & 0x0ffffffff;
        H2 = (H2 + C) & 0x0ffffffff;
        H3 = (H3 + D) & 0x0ffffffff;
        H4 = (H4 + E) & 0x0ffffffff;
    }
    var temp = cvt_hex(H0) + cvt_hex(H1) + cvt_hex(H2) + cvt_hex(H3) + cvt_hex(H4);

    return temp.toLowerCase();
}

function Winrar_format_SHA1(data) {
    if (data.length == 0) { return "\x81\xb7\x3e\xeb\x29\x53\x26\x50\xa3\xf4\x5e\xdc\xd5\xb9\x47\x68\x4c\x3b\xe4\xcd"; }
    else {
        var hex_sha1_digest;
        var sha1_digest = new Uint8Array(20);
        var formated_sha1_digest = "";
        var k = 0;
        hex_sha1_digest = SHA1(data);
        for (k = 0; k < 20; k++) {
            sha1_digest[k] = (Number("0x" + hex_sha1_digest.substring(2 * k, 2 * k + 2))) & 0x0ff;
        }
        for (k = 0; k < 5; k++) {
            formated_sha1_digest += String.fromCharCode(sha1_digest[4 * k + 3]);
            formated_sha1_digest += String.fromCharCode(sha1_digest[4 * k + 2]);
            formated_sha1_digest += String.fromCharCode(sha1_digest[4 * k + 1]);
            formated_sha1_digest += String.fromCharCode(sha1_digest[4 * k + 0]);
        }
        return formated_sha1_digest;
    }
}

function Winrar_get_privkey(data) {
    var d = Winrar_format_SHA1(data);
    var pri_key = "";
    pri_key = pri_key + ((Winrar_format_SHA1("\x01\x00\x00\x00" + d)).substring(0, 2));
    pri_key = pri_key + ((Winrar_format_SHA1("\x02\x00\x00\x00" + d)).substring(0, 2));
    pri_key = pri_key + ((Winrar_format_SHA1("\x03\x00\x00\x00" + d)).substring(0, 2));
    pri_key = pri_key + ((Winrar_format_SHA1("\x04\x00\x00\x00" + d)).substring(0, 2));
    pri_key = pri_key + ((Winrar_format_SHA1("\x05\x00\x00\x00" + d)).substring(0, 2));
    pri_key = pri_key + ((Winrar_format_SHA1("\x06\x00\x00\x00" + d)).substring(0, 2));
    pri_key = pri_key + ((Winrar_format_SHA1("\x07\x00\x00\x00" + d)).substring(0, 2));
    pri_key = pri_key + ((Winrar_format_SHA1("\x08\x00\x00\x00" + d)).substring(0, 2));
    pri_key = pri_key + ((Winrar_format_SHA1("\x09\x00\x00\x00" + d)).substring(0, 2));
    pri_key = pri_key + ((Winrar_format_SHA1("\x0a\x00\x00\x00" + d)).substring(0, 2));
    pri_key = pri_key + ((Winrar_format_SHA1("\x0b\x00\x00\x00" + d)).substring(0, 2));
    pri_key = pri_key + ((Winrar_format_SHA1("\x0c\x00\x00\x00" + d)).substring(0, 2));
    pri_key = pri_key + ((Winrar_format_SHA1("\x0d\x00\x00\x00" + d)).substring(0, 2));
    pri_key = pri_key + ((Winrar_format_SHA1("\x0e\x00\x00\x00" + d)).substring(0, 2));
    pri_key = pri_key + ((Winrar_format_SHA1("\x0f\x00\x00\x00" + d)).substring(0, 2));

    return pri_key;
}

function Winrar_padded_hash(data) {
    return Winrar_format_SHA1(data) + "\x43\x8d\xfd\x0f\x7c\x3c\xe3\xb4\xd1\x1b";
}

function Winrar_get_pubkey(privkey) {
    var Base_Point = 0x0106d197457e485be7873b5ef2224b5a683ca02a73753079c43412318997c98d3d6fdcbc6a27acee0cc2996e0096ae74feb1acf220a2341b898b549440297b8ccn;
    var privkey_num = 0n;
    var pkG = 0n;
    var pkG_x = 0n;
    var pkG_y = 0n;
    var pubk_1 = 0n;
    var pubk_2 = 0n;
    privkey_num = Bytes_to_BigInt(privkey);
    pkG = ECP_smul(privkey_num, Base_Point);
    pkG_x = pkG & (0x07fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffn);
    pkG_y = (pkG >> (255n)) & (0x07fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffn);
    pubk_1 = (2n) * (pkG_x);
    pubk_2 = GF_div(pkG_y, pkG_x) & (1n);
    return pubk_1 + pubk_2;
}

function Winrar_sign(data) {
    var Base_Point = 0x0106d197457e485be7873b5ef2224b5a683ca02a73753079c43412318997c98d3d6fdcbc6a27acee0cc2996e0096ae74feb1acf220a2341b898b549440297b8ccn;
    var winrar_priv_k = 0x059fe6abcca90bdb95f0105271fa85fb9f11f467450c1ae9044b7fd61d65en;
    var order_n = 0x01026dd85081b82314691ced9bbec30547840e4bf72d8b5e0d258442bbcd31n;
    var random = 0n;
    var Random_a = new Uint32Array(2);
    var sign_r = 0n;
    var sign_s = 0n;
    crypto.getRandomValues(Random_a);
    random = ((random + BigInt(Random_a[0])) << (32n));
    random = ((random + BigInt(Random_a[1])));
    random = random & (0x0ffn);
    sign_r = ((order_n << (512n)) + (ECP_smul(random, Base_Point) & (0x07fffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffffn)) + Bytes_to_BigInt(Winrar_padded_hash(data))) % order_n;
    sign_s = ((order_n << (512n)) + random - (winrar_priv_k * sign_r)) % order_n;
    return [sign_r, sign_s];
}

function Winrar_KeyGen(USER, LIC) {
    var temp = "";
    var data = "";
    var data0 = "";
    var data1 = "";
    var data2 = "";
    var data3 = "";
    var data1_r = 0n;
    var data1_s = 0n;
    var data1_rb = "";
    var data1_sb = "";
    var data2_r = 0n;
    var data2_s = 0n;
    var data2_rb = "";
    var data2_sb = "";

    var RAR_UID = "";
    var KEY_STR = "";
    temp = BigInt_to_Bytes(Winrar_get_pubkey(Winrar_get_privkey(USER)), 32);
    data3 = Bytes_to_Hex("\x60" + temp.substring(0, 24));
    data0 = Bytes_to_Hex(BigInt_to_Bytes(Winrar_get_pubkey(Winrar_get_privkey(data3)), 32));
    while (true) {
        var [data1_r, data1_s] = Winrar_sign(LIC);
        if ((data1_r < ((1n) << ((240n) - 1n))) && (data1_s < ((1n) << ((240n) - 1n)))) { break; }
    }
    data1_rb = Bytes_to_Hex(BigInt_to_Bytes(data1_r, 30));
    data1_sb = Bytes_to_Hex(BigInt_to_Bytes(data1_s, 30));
    data1 = "60" + data1_sb + data1_rb;

    while (true) {
    var [data2_r, data2_s] = Winrar_sign(USER + data0);
    if ((data2_r < ((1n) << ((240n) - 1n))) && (data2_s < ((1n) << ((240n) - 1n)))) { break; }
    }
    data2_rb = Bytes_to_Hex(BigInt_to_Bytes(data2_r, 30));
    data2_sb = Bytes_to_Hex(BigInt_to_Bytes(data2_s, 30));
    data2 = "60" + data2_sb + data2_rb;
    data = data0 + data1 + data2 + data3;
    data = "6412212250" + data + ((CRC32(LIC + USER + data).toString(10)).padStart(10, "0"));
    RAR_UID = Bytes_to_Hex(temp.substring(24, 32)) + data0.substring(0, 4);
    KEY_STR = "RAR registration data\n" + USER + "\n" + LIC + "\nUID=" + RAR_UID + "\n";
    KEY_STR = KEY_STR + (data.substring(0, 54)) + "\n";
    KEY_STR = KEY_STR + (data.substring(54, 108)) + "\n";
    KEY_STR = KEY_STR + (data.substring(108, 162)) + "\n";
    KEY_STR = KEY_STR + (data.substring(162, 216)) + "\n";
    KEY_STR = KEY_STR + (data.substring(216, 270)) + "\n";
    KEY_STR = KEY_STR + (data.substring(270, 324)) + "\n";
    KEY_STR = KEY_STR + (data.substring(324, 378)) + "\n";
    return KEY_STR;
}

      
let user = "721PC-Net Corporation";
let lic = "Unlimited Company License";
const key = Winrar_KeyGen(user, lic);
alert(key);
</code>
</pre>


