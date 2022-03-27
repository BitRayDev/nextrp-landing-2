<template>
	<footer class="footer">
    <div class="footer__inner">
      <p class="footer__copyright">
			Устанавливая программу, вы принимаете условия <a href="https://nextrp.ru/#modalOffer">Лицензионного соглашения</a>.<br>
			Все права на товарные знаки принадлежат NEXTRP.<br>
			Как удалить NEXTRP Launcher <a href="https://nextrp.ru/del.html">Инструкция</a>.<br>
			<a href="https://nextrp.ru/#modalPrivacyPolicy">Политика Конфиденциальности</a>.<br>
			© 2021 NEXTRP
		</p>
		<div class="footer__socials">
			<p class="footer__socials-label">Мы в социальных сетях</p>
			<div class="footer__social-icons">
				<a href="https://www.youtube.com/channel/UCCCszAQexNNVOGD9XRG1b-g">
					<img class="footer__social-icon" src="@/assets/img/icons/youtube.svg"/>
				</a>
        <a href="https://vk.com/nextmta">
					<img class="footer__social-icon" src="@/assets/img/icons/vk.svg"/>
				</a>
        <a href="https://t.me/nextrpnews">
					<img class="footer__social-icon" src="@/assets/img/icons/telegram.svg"/>
				</a>
			</div>
		</div>
    </div>
	</footer>
</template>

<script>
export default {};
</script>

<style lang="scss">
.footer {
  font-family: Open Sans;

  background: #000000;
  padding: 2vw 0;
}
.footer__inner {
  display: flex;
  justify-content: space-between;

  width: 60vw;
  margin: 0 auto;
}

.footer__copyright {
  color: #999999;
  font-size: .8vw;

  a {
    text-decoration: underline;
    color: inherit;
  }
}
.footer__socials-label {
  font-size: 1vw;
  font-weight: 700;
  text-transform: uppercase;

  color: #C6C6C6;
}

.footer__social-icons {
  display: flex;
  justify-content: flex-end;
  gap: .5vw;

  margin-top: 1vw;
}
.footer__social-icon {
  height: 2vw;
}
</style>