// load the things we need
var express = require('express');
var app = express();
// var exec = require('child_process').exec;
const { promisify } = require('util');
const exec = promisify(require('child_process').exec)

async function getGitUser () {
  const name = await exec('solana-keygen new --no-passphrase --no-outfile')
  // const email = await exec('git config --global user.email')
  return name
};
// set the view engine to ejs
app.set('view engine', 'ejs');

// use res.render to load up an ejs view file
function execute(command, callback){
    exec(command, function(error, stdout, stderr){ callback(stdout); });
};
// index page 
app.get('/', function(req, res) {
    var mascots = [
        { name: 'Peace', organization: "EcoSysMAAT-KaZimba", birth_year: 1996},
        { name: 'Power', organization: "EcoSysMAAT-SOUL", birth_year: 2001},
        { name: 'Wisdom', organization: "EcoSysMAAT-ACUK", birth_year: 2012}
    ];
    var tagline = "Education for True Global Power";

    res.render('pages/index', {
        mascots: mascots,
        tagline: tagline,
        output:"",
        pubkey:"",
        seedphrase:"",
    });
});

// about page
app.get('/about', function(req, res) {
    res.render('pages/about');
});

app.post('/account/create',async function(req, res) {
    output =await getGitUser()
    // console.log(output)
    str = JSON.stringify(output);
    pubkey = str.split("pubkey:")[1].split("=====")[0].trim()
    pubkey = pubkey.replace("\\n", "");
    seedphrase = str.split("your new keypair:")[1].split("=====")[0].trim()
    seedphrase = seedphrase.replace("\\n", "");
    seedphrase = seedphrase.replace("\\n", "");
    res.render('pages/index',{pubkey:pubkey,seedphrase:seedphrase});
});

app.listen(8080);
console.log('8080 is the magic port');
