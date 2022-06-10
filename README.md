# TInvest-Trading-Assistant-On-Python

## Installation and launch

The script requires Python 3.8 or later installed.

1. Download all files of this repository to a separate folder.

2. Change to the folder and run `pip3 install -r requirements.txt` to install the necessary dependencies.

3. Create a `config.yaml` file in the root of the folder and add an access token to it (you can get it from the link [https://www.tinkoff.ru/invest/settings/](https: //www.tinkoff.ru /invest/settings/)) in the following format:

``yaml
token: t.Dlinnyii_Token_Is_TinkoffAPI
```

4. Run the script with the `python main.py` command. After the initial launch, the settings file will be written to the individual settings for each of your accounts. You can read more about the script and the account settings file in the [Settings file](docs/configuration.md) section.

## Run in Docker

The program is started with the command:

``` hit
docker build -t tinkproject .
docker run --rm -it -v $(pwd):/tinkproject app
```

## Launch parameters

To avoid printing logs, add the `-q` or `--quiet` option when running from the command line.

Or add `-d` or `--debug` for debugging.

Attention: works received as a gift, for example, for an invited friend, may not be processed through the API and will also be absent from the report. Thus, in the presence of donated securities, the final balance of the portfolio will differ from what is indicated in the Tinkoff application.

Securities resulting from a split or possibly some other corporate event may partially be reported as nil.
