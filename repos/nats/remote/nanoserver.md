## `nats:nanoserver`

```console
$ docker pull nats@sha256:cc81cb52f172686a965e1c4e8a55c36dc45bbf434782b00bb9f13b023b4e25c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `nats:nanoserver` - windows version 10.0.17763.1879; amd64

```console
$ docker pull nats@sha256:919213b7bc91d2592c5d1312c0a4afc4191259685c87e5411af02b2f857c7f22
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105629134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c2735946f6f419fec4d9b2c7c5ef0d1de10fcb5bed1024117d3bdecf2ab3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:05:18 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 22 Apr 2021 22:17:39 GMT
RUN cmd /S /C #(nop) COPY file:0bab6ea83b560e32beee362f5586c34607d68bc8fc2e12422611f377373c3392 in C:\nats-server.exe 
# Thu, 22 Apr 2021 22:17:40 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 22 Apr 2021 22:17:41 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 22 Apr 2021 22:17:43 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 22 Apr 2021 22:17:44 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f8d27bfefcaaa84a89f93945c61ccf0af9ad50b1405d9acfa30e9da5ba1fb2db`  
		Last Modified: Wed, 14 Apr 2021 16:10:39 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84508bc2e91e9b08b6992021bcf6575304a72e75fe2e112017331b04d5edc6b8`  
		Last Modified: Thu, 22 Apr 2021 22:32:27 GMT  
		Size: 4.3 MB (4282564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62907c5116573f0b8237cef0b1b52331d4945c3fed33b88e5c961e2f505420a9`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ae9d391bb3e00f300812200277f9faee92744173d7324e3993ef169a0cd1eb`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62014e35aec6648734dd1a046b17cd77df9db4b2f8b17d2272e303ae3b97903a`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908266ff2e3c49a426faa0a3fd232a8d8556b9bd9361c046faaa764058830852`  
		Last Modified: Thu, 22 Apr 2021 22:32:25 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
