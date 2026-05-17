<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trắc nghiệm 60 Từ Vựng B2-C1: Talkshow cùng V (BTS)</title>
    <style>
        * { box-sizing: border-box; }
        body { 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
            background-color: #f3f0f8; /* Nền tím nhạt */
            color: #333; 
            margin: 0; 
            padding: 20px; 
            font-size: 16px; 
        }
        .container { max-width: 95%; margin: 0 auto; } 
        h1 { text-align: center; color: #4a235a; font-size: 1.8em; margin-bottom: 20px; line-height: 1.4;}
        
        /* Bảng điểm ghim trên cùng */
        .score-banner {
            position: sticky;
            top: 10px;
            background: #5b2c6f; /* Tím đậm BTS */
            color: #fff;
            padding: 15px;
            text-align: center;
            font-size: 1.2em;
            font-weight: bold;
            z-index: 100;
            border-radius: 10px;
            margin-bottom: 20px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        }

        /* --- KHUNG CÂU HỎI --- */
        .question-card { 
            background: #fff; 
            border-radius: 12px; 
            padding: 15px; 
            margin-bottom: 15px; 
            box-shadow: 0 4px 8px rgba(0,0,0,0.08); 
            border-top: 5px solid #d4ac0d; /* Viền Vàng Gold */
        }
        .q-header { 
            font-size: 1em; 
            color: #7f8c8d; 
            font-weight: bold; 
            margin-bottom: 10px; 
            text-transform: uppercase;
        }
        .q-word { 
            font-size: 2.5em; 
            font-weight: bold; 
            color: #4a235a; 
            margin-bottom: 15px; 
            text-align: center; 
        }
        
        /* Lưới đáp án */
        .options { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
        @media (max-width: 600px) { .options { grid-template-columns: 1fr; } }
        
        .opt-btn { 
            padding: 15px; font-size: 1.1em; border: 2px solid #d7bde2; 
            border-radius: 8px; background: #fff; cursor: pointer; 
            transition: 0.2s; text-align: center; font-weight: bold; color: #34495e;
        }
        .opt-btn:hover:not(:disabled) { border-color: #5b2c6f; background: #f4ecf7; }
        .opt-btn:disabled { cursor: default; }
        .opt-btn.correct { background: #d4edda; border-color: #28a745; color: #155724; }
        .opt-btn.wrong { background: #f8d7da; border-color: #dc3545; color: #721c24; }
        
        /* --- KHUNG GIẢI THÍCH CHI TIẾT --- */
        .explanation { 
            margin-top: 15px; 
            padding: 15px; 
            border-radius: 8px; 
            background: #fdfefe; 
            border-left: 5px solid #e74c3c; 
            line-height: 1.6;
            animation: fadeIn 0.4s ease-in-out;
            box-shadow: inset 0 0 10px rgba(0,0,0,0.02);
        }

        .correct-ans { 
            color: #c0392b; 
            font-size: 1.3em; 
            display: block; 
            margin-bottom: 8px;
            font-weight: bold;
        }

        .explanation .meaning { 
            margin-bottom: 15px; 
            color: #2c3e50; 
            font-size: 1.15em; 
        }
        
        /* --- KHU VỰC VÍ DỤ --- */
        .example-box {
            background: #f4f6f7; 
            padding: 15px; 
            border-radius: 6px; 
            margin-bottom: 15px; 
            border-left: 4px solid #5b2c6f;
        }
        .example-box .ex-header strong {
            font-size: 1.2em;
            color: #5b2c6f;
        }

        .example-box .kr-ex { 
            font-weight: bold; 
            font-size: 1.4em; 
            color: #8e44ad;
            margin-left: 8px; 
            display: block;
            margin-top: 5px;
            line-height: 1.5;
        }

        .example-box .vn-ex { 
            font-size: 1.15em; 
            color: #34495e; 
            margin-top: 12px;
            border-top: 1px dashed #bdc3c7;
            padding-top: 10px;
        }

        /* --- PHÂN TÍCH HÁN HÀN --- */
        .han-viet-box {
            display: block; 
            background: #fef9e7; 
            color: black; 
            padding: 12px; 
            border-radius: 5px; 
            font-size: 1.15em; 
            border: 1px solid #f1c40f;
        }
        .han-viet-box span { 
            font-weight: bold; 
            color: #b9770e; 
            font-size: 1.1em;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Bài tập Trắc nghiệm: 60 Từ vựng B2-C1<br> (Trích xuất từ Talkshow cùng V - BTS)</h1>
    <div class="score-banner" id="score-text">Điểm: 0 / 0 (Đã làm: 0/60)</div>
    <div id="quiz-container"></div>
</div>

<script>
// Dữ liệu 60 từ vựng đã được tạo câu ví dụ và phân tích chi tiết từ Transcript
const vocabList = [
    { kr: "이목구비", vn: "Ngũ quan, đường nét khuôn mặt", detail: "Tai, mắt, miệng, mũi; dùng để chỉ tổng thể đường nét sắc sảo trên gương mặt.", ex_kr: "눈 5분씩 클로즈업 근접 촬영이 있겠습니다. 이렇게 눈 이목구비를...", ex_vn: "Sẽ có phần quay cận cảnh đôi mắt trong 5 phút. Đường nét khuôn mặt (đôi mắt) thế này...", han: "<span>이목구비</span> (Nhĩ mục khẩu tị: Tai, mắt, miệng, mũi)." },
    { kr: "특임대", vn: "Đội đặc nhiệm", detail: "Lực lượng quân sự được giao nhiệm vụ đặc biệt (Viết tắt của 특수임무대).", ex_kr: "전 특임대에 나왔습니다.", ex_vn: "Em xuất thân từ đội đặc nhiệm (cảnh sát quân sự).", han: "<span>특임대</span> (Đặc nhiệm đội)." },
    { kr: "흠뻑 빠지다", vn: "Đắm chìm, say đắm", detail: "Bị cuốn hút hoàn toàn vào một thứ gì đó, ướt sũng trong cảm xúc.", ex_kr: "아 왜 사람들이 그렇게 얘기하는 줄을... 제가 너무 이 친구의 매력에 흠뻑 빠져서...", ex_vn: "À hiểu tại sao mọi người lại nói như vậy rồi... Do tôi đã quá đắm chìm vào sức hút của người bạn này...", han: "🌱 <span>Từ thuần Hàn (흠뻑: hoàn toàn + 빠지다: rơi vào).</span>" },
    { kr: "얽히다", vn: "Đan xen, gắn liền, vướng mắc", detail: "Các sợi dây rối vào nhau, hoặc các mối quan hệ, câu chuyện liên quan mật thiết.", ex_kr: "오늘 그 위에 얽힌 이야기 BTS의 이야기들을 함께 나눠 보도록 하겠습니다.", ex_vn: "Hôm nay chúng ta sẽ cùng trò chuyện về những câu chuyện gắn liền với cậu ấy và câu chuyện của BTS.", han: "🌱 <span>Từ thuần Hàn.</span>" },
    { kr: "극대화시키다", vn: "Tối đa hóa", detail: "Làm cho cái gì đó đạt đến mức độ lớn nhất, phát huy cao nhất.", ex_kr: "그 맛을 극대화시킬 수 있는 음식을 좀 저도 준비해 봤습니다.", ex_vn: "Tôi cũng đã chuẩn bị một số đồ ăn có thể tối đa hóa (phát huy cao nhất) hương vị đó.", han: "<span>극대화</span> (Cực đại hóa) + <span>시키다</span>." },
    { kr: "로컬리즘", vn: "Tính cục bộ địa phương (Localism)", detail: "Chủ nghĩa địa phương, thường đi kèm với sự chèn ép người ngoài (ma cũ bắt nạt ma mới).", ex_kr: "아, 로컬리즘 텃세가 있었구나.", ex_vn: "À, thì ra là đã có tính địa phương và sự chèn ép (bắt nạt người mới).", han: "💬 <span>Từ ngoại lai (Localism).</span>" },
    { kr: "텃세", vn: "Sự chèn ép, ma cũ bắt nạt ma mới", detail: "Hành động tỏ vẻ bề trên của người ở lâu đối với người mới đến.", ex_kr: "로컬리즘 텃세가 있었구나.", ex_vn: "Thì ra là có tính địa phương và sự chèn ép nhỉ.", han: "🌱 <span>Từ thuần Hàn (터: nền/đất + 세: thế lực).</span>" },
    { kr: "소외감", vn: "Cảm giác bị lạc lõng, xa lánh", detail: "Cảm thấy không thuộc về tập thể, bị bỏ rơi một mình.", ex_kr: "약간 나 혼자 느끼는 소외감 같은 거 있잖아.", ex_vn: "Có chút gì đó giống như cảm giác lạc lõng mà chỉ một mình bản thân cảm nhận được ấy.", han: "<span>소외</span> (Sơ ngoại: xa lánh) + <span>감</span> (Cảm)." },
    { kr: "최고의 경지", vn: "Cảnh giới cao nhất", detail: "Đẳng cấp, mức độ hoàn hảo tột đỉnh trong kỹ năng hoặc nghệ thuật.", ex_kr: "최고의 경지에 올라와 있지 않아도...", ex_vn: "Dù chưa đạt đến cảnh giới cao nhất...", han: "<span>최고</span> (Tối cao) + <span>경지</span> (Cảnh địa)." },
    { kr: "현장", vn: "Hiện trường, tại chỗ", detail: "Nơi một sự việc (quay phim, sân khấu biểu diễn) đang diễn ra.", ex_kr: "많은 무대를 하다 보면은 현장에서 아 실수했다 하면은 일단 호비형 한번 쓱 봐요.", ex_vn: "Biểu diễn nhiều sân khấu rồi nên nếu ở hiện trường (trên sân khấu) mà lỡ làm sai là em liếc nhìn anh J-Hope một cái liền.", han: "<span>현</span> (Hiện) + <span>장</span> (Trường: nơi chốn)." },
    { kr: "무술", vn: "Võ thuật", detail: "Kỹ năng chiến đấu, phòng vệ.", ex_kr: "근데 정말 그런 걸 무술로 배웠어?", ex_vn: "Nhưng mà em thực sự đã học những cái đó như học võ thuật sao?", han: "<span>무</span> (Võ) + <span>술</span> (Thuật)." },
    { kr: "모시다", vn: "Mời, đón tiếp, phụng dưỡng", detail: "Kính ngữ của 데리다 (dẫn theo, mời đến).", ex_kr: "그 주인공 오늘 BTS의 뷔 모시고 이야기 나눠 볼게요.", ex_vn: "Hôm nay chúng ta sẽ mời nhân vật chính là V của BTS đến và cùng trò chuyện nhé.", han: "🌱 <span>Từ thuần Hàn (Kính ngữ).</span>" },
    { kr: "선정되다", vn: "Được chọn, được bình chọn", detail: "Được lựa chọn ra từ nhiều đối tượng khác.", ex_kr: "아름다운 얼굴 1위로 선정되기도 하고 막 그랬잖아요.", ex_vn: "Cậu ấy cũng từng được bình chọn là Gương mặt đẹp trai nhất thế giới số 1 mà.", han: "<span>선정</span> (Tuyển định: chọn ra) + <span>되다</span>." },
    { kr: "근접", vn: "Sự tiếp cận, cận cảnh", detail: "Khoảng cách rất gần (dùng trong quay phim: quay sát mặt).", ex_kr: "눈 5분씩 클로즈업 근접 촬영이 있겠습니다.", ex_vn: "Sẽ có phần quay phim cận cảnh đôi mắt trong 5 phút.", han: "<span>근</span> (Cận: gần) + <span>접</span> (Tiếp: chạm/nối)." },
    { kr: "강렬하다", vn: "Mãnh liệt, cực kỳ mạnh mẽ", detail: "Ấn tượng rất sâu đậm, dữ dội.", ex_kr: "그때 인상이 아주 강렬했거든요.", ex_vn: "Ấn tượng lúc đó thực sự rất mãnh liệt.", han: "<span>강</span> (Cường: mạnh) + <span>렬</span> (Liệt: dữ dội)." },
    { kr: "짜릿하다", vn: "Kích thích, tê rần", detail: "Cảm giác sung sướng, phấn khích nổi da gà.", ex_kr: "무대 위에서 환호를 받을 때 정말 짜릿합니다.", ex_vn: "Lúc nhận được sự hò reo trên sân khấu, cảm giác thực sự rất kích thích (tê rần).", han: "🌱 <span>Từ thuần Hàn.</span>" },
    { kr: "알배추", vn: "Cải thảo non", detail: "Bắp cải thảo nhỏ, giòn ngọt dùng để cuốn thịt.", ex_kr: "알배추랑 같이 먹으면 진짜 맛있어요.", ex_vn: "Ăn cuốn cùng với cải thảo non thì thực sự rất ngon.", han: "🌱 <span>알 (Lõi/hạt) + 배추 (Cải thảo).</span>" },
    { kr: "김장김치", vn: "Kim chi muối (vụ đông)", detail: "Kim chi được muối với số lượng lớn vào mùa đông.", ex_kr: "김장김치 가져왔는데 한 번 드셔보세요.", ex_vn: "Em có mang theo kim chi mới muối đến, anh ăn thử một lần xem sao.", han: "<span>김장</span> (Việc muối kim chi) + <span>김치</span>." },
    { kr: "손이 크다", vn: "(Nghĩa bóng) Hào phóng, làm số lượng lớn", detail: "Thường chỉ người hay nấu ăn nhiều, cho đi rộng rãi.", ex_kr: "저희 할머니가 손이 좀 크셔 가지고...", ex_vn: "Vì bà ngoại em rất hào phóng (hay làm đồ ăn siêu nhiều) nên...", han: "🌱 <span>Thành ngữ thuần Hàn (손: tay + 크다: lớn).</span>" },
    { kr: "간장게장", vn: "Cua ngâm nước tương", detail: "Món ăn truyền thống dọn kèm cơm trắng của Hàn Quốc.", ex_kr: "간장게장이 진짜 밥도둑이거든요.", ex_vn: "Cua ngâm nước tương đúng thật là kẻ trộm cơm mà.", han: "<span>간장</span> (Kiến tương: nước tương) + <span>게장</span> (Cua ngâm)." },
    { kr: "취향 저격", vn: "Đúng gu, hợp sở thích hoàn toàn", detail: "Đánh trúng vào sở thích cá nhân.", ex_kr: "이거 완전 취향 저격인데.", ex_vn: "Cái này hoàn toàn đánh trúng gu của anh luôn đấy.", han: "<span>취향</span> (Thú hướng: sở thích) + <span>저격</span> (Thư kích: bắn trúng)." },
    { kr: "들키다", vn: "Bị phát hiện, bị lộ tẩy", detail: "Làm việc lén lút bị người khác bắt gặp.", ex_kr: "몰래 먹다가 들켰어요.", ex_vn: "Đang ăn lén thì bị phát hiện mất.", han: "🌱 <span>Từ thuần Hàn.</span>" },
    { kr: "관자", vn: "Cồi sò điệp", detail: "Phần cồi thịt của con sò điệp.", ex_kr: "관자랑 전복이랑 사왔어.", ex_vn: "Em đã mua cồi sò điệp và bào ngư đến.", han: "<span>관자</span> (Quán tử)." },
    { kr: "전복", vn: "Bào ngư", detail: "Một loại hải sản cao cấp, rất bổ dưỡng.", ex_kr: "관자랑 전복이랑 사왔어.", ex_vn: "Em đã mua cồi sò điệp và bào ngư đến.", han: "<span>전복</span> (Toàn phúc)." },
    { kr: "부근", vn: "Khoảng thời gian đó, khu vực lân cận", detail: "Xung quanh một mốc thời gian hoặc địa điểm.", ex_kr: "그 시기 부근에 제가 참 고민이 많았습니다.", ex_vn: "Vào khoảng thời gian đó, em đã có rất nhiều trăn trở.", han: "<span>부</span> (Phụ: gần) + <span>근</span> (Cận: gần)." },
    { kr: "빡빡하다", vn: "Kín mít, chật vật, dày đặc", detail: "Không có kẽ hở (lịch trình) hoặc tình hình tài chính/cuộc sống khó khăn.", ex_kr: "스케줄이 되게 빡빡해서...", ex_vn: "Vì lịch trình rất dày đặc (kín mít)...", han: "🌱 <span>Từ thuần Hàn.</span>" },
    { kr: "대표적", vn: "Mang tính tiêu biểu, đại diện", detail: "Điển hình nhất cho một nhóm hoặc tình huống.", ex_kr: "했다가 안 된 케이스. 저는 된 케이스. 그게 가장 대표적인 케이스죠.", ex_vn: "Trường hợp muốn làm mà không được. Và trường hợp của em là được. Đó chính là trường hợp tiêu biểu nhất.", han: "<span>대</span> (Đại) + <span>표</span> (Biểu) + <span>적</span> (Đích)." },
    { kr: "현수막", vn: "Băng rôn, cờ phướn", detail: "Tấm vải in chữ để chúc mừng, thông báo.", ex_kr: "요즘에는 거창에 현수막에 제가 걸린다고...", ex_vn: "Nghe bảo dạo này ở Geochang người ta treo băng rôn có hình em...", han: "<span>현수막</span> (Huyền thù mạc)." },
    { kr: "납득하다", vn: "Hiểu ra, chấp nhận, bị thuyết phục", detail: "Thấu hiểu lý do và chấp nhận một sự việc.", ex_kr: "그래서 제가 납득했죠. 해 버렸죠.", ex_vn: "Nên em đã hiểu ra và chấp nhận. Em đã làm điều đó luôn.", han: "<span>납득</span> (Nạp đắc: thu nhận) + <span>하다</span>." },
    { kr: "놀라울 정도", vn: "Đến mức đáng ngạc nhiên", detail: "Gây kinh ngạc vì sự thay đổi hoặc mức độ vượt bậc.", ex_kr: "정말 놀라울 정도로 성장했어요.", ex_vn: "Đã trưởng thành đến mức đáng ngạc nhiên.", han: "🌱 <span>놀랍다 (Ngạc nhiên) + 정도 (Mức độ).</span>" },
    { kr: "상경하다", vn: "Lên thủ đô (Seoul)", detail: "Đi từ tỉnh lẻ lên thủ đô để sinh sống/học tập.", ex_kr: "고등학교를 이제 상경해서 서울로...", ex_vn: "Lên cấp 3 thì em bắt đầu lên Seoul (thủ đô)...", han: "<span>상경</span> (Thượng kinh) + <span>하다</span>." },
    { kr: "훈장", vn: "Huân chương", detail: "Phần thưởng cao quý của nhà nước.", ex_kr: "너 훈장 받았잖아. 그지?", ex_vn: "Em đã nhận được huân chương mà. Đúng không?", han: "<span>훈장</span> (Huân chương)." },
    { kr: "꿈을 접다", vn: "Từ bỏ ước mơ, gác lại hoài bão", detail: "Quyết định không theo đuổi ước mơ nữa.", ex_kr: "아버지가 꿈을 접으시고 저를 밀어주셨죠.", ex_vn: "Bố em đã gác lại ước mơ của mình và hậu thuẫn cho em.", han: "🌱 <span>꿈 (Ước mơ) + 접다 (Gấp lại).</span>" },
    { kr: "베테랑", vn: "Lão làng, người dày dặn kinh nghiệm", detail: "Chuyên gia, người có kỹ năng điêu luyện trong nghề.", ex_kr: "표정은 되게 베테랑이네.", ex_vn: "Biểu cảm đúng là rất sành sỏi (lão làng) nhỉ.", han: "💬 <span>Từ ngoại lai (Veteran).</span>" },
    { kr: "나름", vn: "Theo cách riêng, tùy thuộc", detail: "Một mức độ riêng biệt nào đó của bản thân.", ex_kr: "저도 나름대로 열심히 준비했습니다.", ex_vn: "Em cũng đã chuẩn bị chăm chỉ theo cách riêng của mình.", han: "🌱 <span>Từ thuần Hàn.</span>" },
    { kr: "실천으로 옮기다", vn: "Đưa vào thực tiễn, thực hiện", detail: "Biến suy nghĩ hoặc kế hoạch thành hành động.", ex_kr: "꿈을 한번 실천으로 옮기고 싶다.", ex_vn: "Em muốn thử đưa giấc mơ chuyển thành hành động thực tế.", han: "<span>실천</span> (Thực tiễn) + <span>으로 옮기다</span> (Chuyển sang)." },
    { kr: "예술고등학교", vn: "Trường trung học nghệ thuật", detail: "Trường cấp 3 chuyên đào tạo nghệ thuật (thường gọi tắt là 예고).", ex_kr: "제가 예술고등학교에 진학하고 싶어서...", ex_vn: "Bởi vì em muốn thi vào trường trung học nghệ thuật...", han: "<span>예술</span> (Nghệ thuật) + <span>고등학교</span> (Cấp 3)." },
    { kr: "가능성", vn: "Khả năng, tiềm năng", detail: "Xác suất thành công hoặc tiềm năng phát triển.", ex_kr: "거기는 들어가야지 이제 좀 가능성이 보인다고 하더라.", ex_vn: "Người ta bảo là phải vào được (trường) đó thì mới nhìn thấy chút khả năng.", han: "<span>가능성</span> (Khả năng tính)." },
    { kr: "전략적", vn: "Mang tính chiến lược", detail: "Có kế hoạch bài bản hướng tới mục tiêu.", ex_kr: "입시는 그렇게 전략적이어야 해.", ex_vn: "Kỳ thi tuyển sinh là phải mang tính chiến lược như thế đấy.", han: "<span>전략</span> (Chiến lược) + <span>적</span> (Đích)." },
    { kr: "입시", vn: "Thi tuyển sinh", detail: "Kỳ thi đầu vào cấp 3 hoặc đại học.", ex_kr: "입시는 그렇게 전략적이어야 해.", ex_vn: "Thi tuyển sinh là phải mang tính chiến lược như thế.", han: "<span>입시</span> (Nhập thí: Thi vào)." },
    { kr: "레슨비", vn: "Tiền học phí, tiền học gia sư", detail: "Tiền trả cho các buổi học kỹ năng riêng (âm nhạc, vũ đạo...).", ex_kr: "당시 레슨비가 만만치 않았거든요.", ex_vn: "Tiền học phí lúc bấy giờ không hề rẻ một chút nào.", han: "💬 <span>Lesson + 비 (Phí).</span>" },
    { kr: "귀하다", vn: "Quý giá, đáng trân trọng", detail: "Có giá trị cao, hiếm có.", ex_kr: "정말 귀한 시간 내주셔서 감사합니다.", ex_vn: "Cảm ơn vì đã dành thời gian quý báu cho chúng tôi.", han: "<span>귀</span> (Quý) + <span>하다</span>." },
    { kr: "막강하다", vn: "Hùng mạnh, đáng gờm", detail: "Sức mạnh rất lớn, không dễ đối phó.", ex_kr: "저보다 더 막강한 친구가 있었나 봐요.", ex_vn: "Có vẻ như đã có một người bạn (đối thủ) đáng gờm hơn em.", han: "<span>막강</span> (Mạc cường) + <span>하다</span>." },
    { kr: "비공개 오디션", vn: "Buổi thử giọng kín", detail: "Buổi casting không công khai ra bên ngoài.", ex_kr: "거기에서 비공개 오디션이 있었습니다.", ex_vn: "Ở đó đã diễn ra một buổi thử giọng (audition) không công khai.", han: "<span>비공개</span> (Phi công khai) + <span>Audition</span>." },
    { kr: "형편없다", vn: "Tồi tệ, không ra gì", detail: "Chất lượng hoặc năng lực vô cùng kém cỏi.", ex_kr: "그때 제 실력은 형편이 없었었거든요.", ex_vn: "Lúc đó thực lực của em rất tồi tệ (không ra gì).", han: "🌱 <span>Từ thuần Hàn (형편: hoàn cảnh + 없다).</span>" },
    { kr: "개다리 춤", vn: "Điệu nhảy chân ghẻ/chân cào", detail: "Điệu nhảy hài hước gập đầu gối rung rung đặc trưng của Hàn Quốc.", ex_kr: "설날이나 명절에 이제 개다리 춤추고...", ex_vn: "Vào ngày Seollal hay dịp lễ tết là em nhảy điệu chân chó...", han: "🌱 <span>개 (Chó) + 다리 (Chân) + 춤 (Nhảy).</span>" },
    { kr: "경력", vn: "Kinh nghiệm, bề dày hoạt động", detail: "Quá trình làm việc trong một lĩnh vực.", ex_kr: "그게 제 첫 경력이었습니다.", ex_vn: "Đó chính là kinh nghiệm (hoạt động) đầu tiên của em.", han: "<span>경력</span> (Kinh lịch)." },
    { kr: "궁극적으로", vn: "Một cách tận cùng, cuối cùng thì", detail: "Đích đến cuối cùng của một mục đích sâu xa.", ex_kr: "궁극적으로 제가 하고 싶은 음악은...", ex_vn: "Mục đích cuối cùng, âm nhạc mà em muốn làm là...", han: "<span>궁극</span> (Cùng cực: tận cùng) + <span>적</span> + <span>으로</span>." },
    { kr: "검토하다", vn: "Xem xét, rà soát", detail: "Kiểm tra kỹ lưỡng lại nội dung hoặc kế hoạch.", ex_kr: "회사에서 검토를 좀 심각하게 한 다음에...", ex_vn: "Sau khi công ty xem xét một cách khá nghiêm túc...", han: "<span>검토</span> (Kiểm thảo) + <span>하다</span>." },
    { kr: "긍정적", vn: "Tích cực", detail: "Hướng về khía cạnh tốt đẹp, thái độ chấp thuận.", ex_kr: "반응이 썩 그렇게 긍정적이진 않으셨어요.", ex_vn: "Phản ứng của họ không hẳn là quá tích cực đâu.", han: "<span>긍정</span> (Khẳng định) + <span>적</span> (Đích)." },
    { kr: "중소 기획사", vn: "Công ty giải trí quy mô vừa và nhỏ", detail: "Các công ty quản lý nghệ sĩ không thuộc top các ông lớn.", ex_kr: "그때는 저희가 중소 기획사였으니까요.", ex_vn: "Vì lúc bấy giờ chúng em chỉ là một công ty giải trí vừa và nhỏ thôi.", han: "<span>중소</span> (Trung tiểu) + <span>기획사</span>." },
    { kr: "대형 기획사", vn: "Công ty giải trí quy mô lớn", detail: "Các công ty giải trí khổng lồ (như BIG3/HYBE).", ex_kr: "매출이 대형이 아니야. 대형 기획사가 아니었잖아요.", ex_vn: "Doanh thu không thuộc quy mô lớn. Lúc đó không phải là công ty giải trí lớn mà.", han: "<span>대형</span> (Đại hình) + <span>기획사</span>." },
    { kr: "화제성", vn: "Sức hút dư luận, tính chủ đề", detail: "Mức độ thu hút sự chú ý và bàn tán của công chúng.", ex_kr: "관심도가 있거나 아니면은 좀 되게 화제성이 필요했던 시기였어요.", ex_vn: "Đó là thời kỳ mà chúng em rất cần mức độ quan tâm hoặc tính chủ đề (sức hút dư luận).", han: "<span>화제</span> (Thoại đề) + <span>성</span> (Tính)." },
    { kr: "돌파구", vn: "Lối thoát, bước đột phá", detail: "Giải pháp vượt qua tình trạng bế tắc.", ex_kr: "그게 저희만의 돌파구였죠.", ex_vn: "Đó chính là bước đột phá (lối thoát) của riêng chúng em.", han: "<span>돌파</span> (Đột phá) + <span>구</span> (Khẩu: cửa)." },
    { kr: "방출하다", vn: "Tỏa ra, phát ra (năng lượng, sức hút)", detail: "Giải phóng, thể hiện hết những gì mình có ra ngoài.", ex_kr: "저의 매력을 어디에다가 방출은 하고 싶은데...", ex_vn: "Em muốn giải phóng (tỏa ra) sức hút của mình ở đâu đó...", han: "<span>방출</span> (Phóng xuất) + <span>하다</span>." },
    { kr: "페르소나", vn: "Vỏ bọc, nhân cách thể hiện ra ngoài (Persona)", detail: "Hình ảnh hoặc mặt nạ xã hội mà một người tự tạo ra để giao tiếp.", ex_kr: "그냥 하나의 페르소나 만드는 거를 좋아하나 봐요.", ex_vn: "Có vẻ như em rất thích việc tạo ra một vỏ bọc (nhân cách thể hiện) cho riêng mình.", han: "💬 <span>Từ ngoại lai (Persona).</span>" },
    { kr: "몰입하다", vn: "Đắm chìm, tập trung cao độ", detail: "Dồn hết sự tập trung vào một việc hoặc một vai diễn.", ex_kr: "몰입해서 한다는 거를 워낙 약간 익숙해져 있기도 하고...", ex_vn: "Việc tập trung cao độ đắm chìm vào công việc vốn dĩ em cũng đã khá quen rồi...", han: "<span>몰입</span> (Một nhập: chìm đắm) + <span>하다</span>." },
    { kr: "매듭", vn: "Nút thắt", detail: "Phần buộc lại của dây, hoặc điểm kết thúc của một sự việc.", ex_kr: "이렇게 하면은 매듭이 된다라는 거를...", ex_vn: "Việc nếu làm thế này sẽ tạo thành một nút thắt...", han: "🌱 <span>Từ thuần Hàn.</span>" },
    { kr: "발향", vn: "Sự tỏa hương", detail: "Sự lan tỏa mùi hương của nến thơm, nước hoa.", ex_kr: "이게 발향이 진짜 좋거든요.", ex_vn: "Cái này độ tỏa hương thực sự rất tốt đấy ạ.", han: "<span>발향</span> (Phát hương)." },
    { kr: "알맹이", vn: "Ruột, phần lõi, phần cốt lõi", detail: "Phần nhân bên trong (trong ngữ cảnh này V nói đùa về chiếc đĩa CD thật nằm bên trong vỏ hộp).", ex_kr: "나중에 제가 이거 알맹이 들고 오겠습니다.", ex_vn: "Lát nữa em sẽ mang cái lõi (chiếc đĩa CD thật) đến ạ.", han: "🌱 <span>Từ thuần Hàn.</span>" }
];

// Trộn mảng 60 từ
vocabList.sort(() => 0.5 - Math.random());

// Tạo cấu trúc câu hỏi
const quizData = vocabList.map((item, index) => {
    let pool = vocabList.filter((_, i) => i !== index);
    pool.sort(() => 0.5 - Math.random());
    let distractors = [pool[0].vn, pool[1].vn, pool[2].vn];
    
    let options = [...distractors, item.vn];
    options.sort(() => 0.5 - Math.random());
    
    return {
        kr: item.kr,
        options: options,
        correctIndex: options.indexOf(item.vn),
        answerText: item.vn,
        detail: item.detail,
        ex_kr: item.ex_kr,
        ex_vn: item.ex_vn,
        han: item.han
    };
});

let score = 0;
let answeredCount = 0;
const container = document.getElementById('quiz-container');

function renderQuiz() {
    let html = '';
    quizData.forEach((q, qIndex) => {
        html += `
        <div class="question-card" id="q-card-${qIndex}">
            <div class="q-header">Câu ${qIndex + 1} / 60</div>
            <div class="q-word">${q.kr}</div>
            <div class="options" id="opts-${qIndex}">
                ${q.options.map((opt, oIndex) => `
                    <button class="opt-btn" onclick="checkAns(${qIndex}, ${oIndex}, this)">${opt}</button>
                `).join('')}
            </div>
            
            <div class="explanation" id="exp-${qIndex}" style="display:none;">
                <strong class="correct-ans">✅ Đáp án đúng: ${q.answerText}</strong>
                <div class="meaning"><em>Giải nghĩa:</em> ${q.detail}</div>
                
                <div class="example-box">
                    <div class="ex-header">
                        📖 <strong>Ví dụ (trích từ Talkshow):</strong> 
                        <span class="kr-ex">"${q.ex_kr}"</span>
                    </div>
                    <div class="vn-ex">➔ ${q.ex_vn}</div>
                </div>

                <div class="han-viet-box">🔍 <strong>Phân tích:</strong> ${q.han}</div>
            </div>
        </div>
        `;
    });
    container.innerHTML = html;
}

function checkAns(qIndex, selectedIndex, btnElement) {
    const q = quizData[qIndex];
    const optionsDiv = document.getElementById(`opts-${qIndex}`);
    const buttons = optionsDiv.querySelectorAll('.opt-btn');
    
    buttons.forEach((btn, idx) => {
        btn.disabled = true;
        if (idx === q.correctIndex) {
            btn.classList.add('correct');
        } else if (idx === selectedIndex) {
            btn.classList.add('wrong');
        }
    });
    
    answeredCount++;
    if (selectedIndex === q.correctIndex) {
        score++;
    }
    
    document.getElementById('score-text').innerText = `Điểm: ${score} / ${answeredCount} (Đã làm: ${answeredCount}/60)`;
    document.getElementById(`exp-${qIndex}`).style.display = 'block';
}

window.onload = renderQuiz;
</script>

</body>
</html>
