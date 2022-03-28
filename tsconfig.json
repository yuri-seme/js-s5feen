// /public/javascript.js

// Get the current username from the cookies
var user = cookie.get('user');
if (!user) {

  // Ask for the username if there is none set already
  user = prompt('Choose a username:');
  if (!user) {
    alert('We cannot work with you like that!');
  } else {
    // Store it in the cookies for future use
    cookie.set('user', user);
  }
}
var socket = io();
socket.on('count', function (data) {
  $('.user-count').html(data);
});
socket.on('message', function (data) {
  $('.chat').append('<p><strong>' + data.user + '</strong>: ' + data.message + '</p>');
});
$('form').submit(function (e) {
  var message = $(e.target).find('input').val();
  socket.emit('message', {
    user: cookie.get('user') || 'Anonymous',
    message: message
    e.target.reset();
    $(e.target).find('input').focus();
    var user = cookie.get('user');
if (!user) {
  user = prompt('Choose a username:');
  if (!user) {
    alert('We cannot work with you like that!');
  } else {
    cookie.set('user', user);
    var socket = io();
    socket.on('count', function (data) {
      $('.user-count').html(data);
      socket.on('message', function (data) {
        $('.chat').append('<p><strong>' + data.user + '</strong>: ' + data.message + '</p>');
        $('form').submit(function (e) {
          e.preventDefault();
          var message = $(e.target).find('input').val();
          socket.emit('message', {
            user: cookie.get('user') || 'Anonymous',
            message: message
            e.target.reset();
  $(e.target).find('input').focus();
  const server = require('server');
const { get, socket } = server.router;
const { render } = server.reply;

server([
  get('/', ctx => render('index.html'))
  const server = require('server');
const { get, socket } = server.router;
const { render } = server.reply;

const updateCounter = ctx => {
  ctx.io.emit('count', ctx.io.sockets.sockets.length);
  server
  get('/', ctx => render('index.html')),
  socket('connect', updateCounter),
  socket('disconnect', updateCounter)
  const server = require('server');
const { get, socket } = server.router;
const { render } = server.reply;
const updateCounter = ctx => {
  ctx.io.emit('count', Object.keys(ctx.io.sockets.sockets).length);
  const sendMessage = ctx => {
    ctx.io.emit('message', ctx.data);
    server([
      get('/', ctx => render('index.html')),
      socket('connect', updateCounter),
      socket('disconnect', updateCounter),
      socket('message', sendMessage)