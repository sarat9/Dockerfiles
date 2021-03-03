
#Docker file to run Angular app in Dev Mode


Running production mode on Node is not recommended. Use expressjs or another server instead.

CMD ["ng", "serve", "--host", "0.0.0.0", "--port", "4202","--prod"]

If deploying on any Cloud Server such as AWS, you might require to disable the host check or set the public host as your host IP. Else it might give you invalid host header error response.

CMD ["ng", "serve", "--host", "0.0.0.0", "--port", "4202", "--disable-host-check", "--prod"]

or

CMD ["ng", "serve", "--host", "0.0.0.0", "--port", "4202", "--publicHost", "your-host-ip-port-or-your-host.com", "--prod"]

