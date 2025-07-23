
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";
import { Avatar, AvatarFallback, AvatarImage } from "@/components/ui/avatar";
import { Button } from "@/components/ui/button";
import { useState } from "react";

const Index = () => {
  const [showHiddenSkill, setShowHiddenSkill] = useState(false);
  const [showQuirks, setShowQuirks] = useState(false);
  const [showEmbarrassing, setShowEmbarrassing] = useState(false);

  return (
    <div className="min-h-screen bg-gradient-to-br from-pink-100 to-rose-200 py-12 px-4 sm:px-6">
      <div className="max-w-4xl mx-auto">
        {/* 个人信息头部 */}
        <div className="text-center mb-12">
          <h1 className="text-4xl md:text-5xl font-bold text-pink-700 mb-4" style={{ fontFamily: "KaiTi, serif" }}>
            ✨ 小太阳 ✨
          </h1>
          <p className="text-xl text-gray-600 max-w-2xl mx-auto">
            🎓 正在努力成为AI产品经理的追梦人
          </p>
        </div>

        {/* 照片展示 */}
        <Card className="mb-12">
          <CardHeader>
            <CardTitle className="text-xl flex items-center">
              📸 我的靓照
            </CardTitle>
          </CardHeader>
          <CardContent>
            <img 
              src="/Users/lingyizhu/Downloads/1df1094db53926191f52bd3f9929b6f7.JPG" 
              alt="我的照片" 
              className="rounded-lg mx-auto object-cover w-full h-96"
            />
          </CardContent>
        </Card>

        {/* 美食最爱 */}
        <Card className="mb-12">
          <CardHeader>
            <CardTitle className="text-xl flex items-center">
              🍖 我的美食最爱
            </CardTitle>
          </CardHeader>
          <CardContent>
            <div className="flex flex-col items-center">
              <img 
                src="https://nocode.meituan.com/photo/search?keyword=bbq&width=600&height=400" 
                alt="最爱的烤肉" 
                className="rounded-lg mx-auto object-cover w-full h-64 mb-4"
              />
              <p className="text-lg text-center">
                没有烤肉的夏天是不完整的！<span className="font-bold text-red-500">滋滋作响的烤肉才是灵魂伴侣！🥩</span>
              </p>
            </div>
          </CardContent>
        </Card>

        {/* 兴趣爱好 */}
        <Card className="mb-12">
          <CardHeader>
            <CardTitle className="text-xl flex items-center">
              🎮 学习之余，我最大的爱好是...
            </CardTitle>
          </CardHeader>
          <CardContent>
            <div className="flex flex-col md:flex-row items-center gap-8">
              <img 
                src="https://nocode.meituan.com/photo/search?keyword=gaming&width=600&height=400" 
                alt="我的爱好" 
                className="rounded-lg mx-auto object-cover w-full md:w-1/2 h-64"
              />
              <div className="text-lg md:text-xl">
                <p className="mb-2">放下书本，我就会立刻投身于</p>
                <p className="font-bold text-purple-600 mb-2">唱歌和打游戏</p>
                <p>最常玩的游戏是 <span className="font-bold text-orange-500">守望先锋</span>！</p>
              </div>
            </div>
          </CardContent>
        </Card>

        {/* 个人信息卡片 */}
        <div className="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12">
          {/* 小标签 */}
          <Card>
            <CardHeader>
              <CardTitle className="text-xl flex items-center">
                🔮 关于我的一些"小标签"
              </CardTitle>
            </CardHeader>
            <CardContent>
              <div className="space-y-4">
                <div>
                  <p className="font-medium">星座：</p>
                  <p className="text-lg">♉️ 固执又温柔的金牛座，像老牛一样踏实前行</p>
                </div>
                <div>
                  <p className="font-medium">MBTI：</p>
                  <p className="text-lg">🔧 ISTP，动手达人就是我！喜欢把想法变成现实</p>
                </div>
              </div>
            </CardContent>
          </Card>

          {/* 隐藏技能 */}
          <Card>
            <CardHeader>
              <CardTitle className="text-xl flex items-center">
                🤫 我的隐藏技能
              </CardTitle>
            </CardHeader>
            <CardContent>
              {/* 移除按钮和内容，只保留标题 */}
            </CardContent>
          </Card>
        </div>

        {/* 糗事和小缺点 - 拆分为两张独立卡片 */}
        <div className="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12">
          {/* 糗事卡片 */}
          <Card>
            <CardHeader>
              <CardTitle className="text-xl flex items-center">
                😅 让我记忆犹新的糗事
              </CardTitle>
            </CardHeader>
            <CardContent>
              <Button 
                onClick={() => setShowEmbarrassing(!showEmbarrassing)}
                variant="outline"
                className="mb-4"
              >
                {showEmbarrassing ? "收起" : "点击查看糗事"}
              </Button>
              {showEmbarrassing && (
                <div className="animate-in fade-in duration-300">
                  <p className="text-lg">
                    在第一年留学的时候跟朋友购物，在结账时收银员问我：How's your day today, 我听成了How's your date, 并说我不是同性恋，没有在dating😂
                  </p>
                </div>
              )}
            </CardContent>
          </Card>

          {/* 小缺点卡片 */}
          <Card>
            <CardHeader>
              <CardTitle className="text-xl flex items-center">
                🙈 我的小缺点
              </CardTitle>
            </CardHeader>
            <CardContent>
              <Button 
                onClick={() => setShowQuirks(!showQuirks)}
                variant="outline"
                className="mb-4"
              >
                {showQuirks ? "收起" : "点击查看缺点"}
              </Button>
              {showQuirks && (
                <div className="animate-in fade-in duration-300">
                  <p className="text-lg">
                    人无完人嘛，我承认我是 <span className="font-bold text-purple-500">重度懒癌患者</span>！
                    能躺着绝不坐着，能坐着绝不站着，沙发就是我的第二个家～
                    每次周末计划要早起学习，结果都在床上和被子缠绵到中午😴
                  </p>
                </div>
              )}
            </CardContent>
          </Card>
        </div>

        {/* 未来寄语 */}
        <Card className="bg-gradient-to-r from-pink-100 to-rose-100 border-0">
          <CardHeader>
            <CardTitle className="text-xl flex items-center">
              💌 对 2026 年的自己说句话
            </CardTitle>
          </CardHeader>
          <CardContent>
            <div className="flex flex-col items-center text-center">
              <p className="text-2xl font-bold text-pink-700">
                "Hi，一年后的我，希望你已经成为一名出色的AI产品经理，并且游戏技术更上一层楼！🎮"
              </p>
            </div>
          </CardContent>
        </Card>
      </div>
    </div>
  );
};

export default Index;
