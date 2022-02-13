// 1. Отправить запрос.
// 2. Статус код 200

pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

// 3. Проверить, что в body приходит правильный string.


pm.test("Good string", function () {
    pm.expect(pm.response.text()).to.include("This is the first responce from server!");
});
