var Discordie = require('discordie')

const Events = Dicordie.Events;
const client = new Discordie();

client.connect({
  token: 'MzcyNTgxNjIzMTIxODM4MDkx.DNGRdg.D54koxdQtzUUEv51RWZ4u4Ny-oc'
  });
  
  client.Dispatcher.on(Events.MESSAGE_CREATE, e => {
    console. log('Connected as: ' + client.User.Username);
  });
  
  client.Dispatcher.on(Events.MESSAGE_CREATE, e => {
    if (e.message.content == 'PING') {
      e.message.channel.sendMessage('PONG');
    }
  });
  
