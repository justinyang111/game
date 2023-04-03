// 定义游戏变量
var canvas, context, objects, player, bullets, enemies, score;

// 初始化游戏
function initGame() {
	canvas = document.getElementById("gameCanvas");
	context = canvas.getContext("2d");

	objects = [];
	bullets = [];
	enemies = [];
	score = 0;

	player = new Player(canvas.width/2, canvas.height - 50, 30, 30, 5);
	objects.push(player);

	// 创建敌人
	for (var i = 0; i < 10; i++) {
		var enemy = new Enemy(Math.random() * (canvas.width - 30), -30, 30, 30, 2);
		objects.push(enemy);
		enemies.push(enemy);
	}
}

// 更新游戏
function updateGame() {
	// 清除画布
	context.clearRect(0, 0, canvas.width, canvas.height);

	// 更新游戏对象
	for (var i in objects) {
		var object = objects[i];
		object.update();

		// 删除越界的子弹和敌人
		if (object.type == "bullet" && (object.y < -30 || object.y > canvas.height)) {
			objects.splice(i, 1);
			bullets.splice(bullets.indexOf(object), 1);
		}
		if (object.type == "enemy" && (object.y > canvas.height)) {
			objects.splice(i, 1);
			enemies.splice(enemies.indexOf(object), 1);
		}
	}

	// 检测子弹与敌人的碰撞
	for (var i in bullets) {
		var bullet = bullets[i];
		for (var j in enemies) {
			var enemy = enemies[j];
			if (bullet.collidesWith(enemy)) {
				// 删除击中的子弹和敌人
				objects.splice(objects.indexOf(bullet), 1);
				objects.splice(objects.indexOf(enemy), 1);
				bullets.splice(i, 1);
				enemies.splice(j, 1);

				// 增加分数
				score += 10;
			}
		}
	}

	// 绘制分数
	context.fillStyle = "black";
	context.font = "bold 20px sans-serif";
	context.fillText("Score: " + score, 10, 30);

	// 检测玩家与敌人的碰撞
	for (var i in enemies) {
		var enemy = enemies[i];
		if (player.collidesWith(enemy)) {
			alert("Game Over! Your score is " + score);
			location.reload();
		}
	}
}

// 定义玩家类
class Player {
	constructor(x, y, width, height, speed) {
		this.x = x;
		this.y = y;
		this.width = width;
		this.height = height;
		this.speed = speed;
		this.type = "player";
	}

	update() {
		// 移动玩家
		if (37 in keysDown) {
			this.x -= this.speed;
		}
		if (39 in keysDown) {
			this.x += this.speed;
		}

		// 限制玩家移动范围
		if (this.x < 0) {
			this.x = 0;
		}
		if (this.x > canvas.width - this.width) {
			this.x = canvas.width - this.width;
		}

		// 绘制玩家
		context.fillStyle = "blue";
		context.fillRect(this.x, this.y, this.width, this.height);
	}

	// 碰撞检测
	collidesWith(object) {
		if (this.x + this.width < object.x || this.x > object.x + object.width || this.y + this.height < object.y || this.y > object.y + object.height) {
			return false;
		}
		return true;
	}
}

// 定义敌人类
class Enemy {
	constructor(x, y, width, height, speed) {
		this.x = x;
		this.y = y;
		this.width = width;
		this.height = height;
		this.speed = speed;
		this.type = "enemy";
	}

	update() {
		// 移动敌人
		this.y += this.speed;

		// 绘制敌人
		context.fillStyle = "red";
		context.fillRect(this.x, this.y, this.width, this.height);
	}

	// 碰撞检测
	collidesWith(object) {
		if (this.x + this.width < object.x || this.x > object.x + object.width || this.y + this.height < object.y || this.y > object.y + object.height) {
			return false;
		}
		return true;
	}
}

// 处理键盘事件
var keysDown = {};
window.addEventListener("keydown", function(event) {
	keysDown[event.keyCode] = true;
});

window.addEventListener("keyup", function(event) {
	delete keysDown[event.keyCode];
});

// 开始游戏
initGame();
setInterval(updateGame, 30);
