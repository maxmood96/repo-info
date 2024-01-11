## `mongo:6-nanoserver-1809`

```console
$ docker pull mongo@sha256:0e14037c133f4ebd0d44d08b1e41093905b8dfbbe129e6a729325aa48b6a8261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `mongo:6-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull mongo@sha256:75bf9db1a6f6c3cb566001986af515194a3f123db83b78f575c9f2a0a5fe9f60
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.4 MB (622405232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d2e8715c942a4d7291d43c129cbbb2cc62f162fc40c9cf135b21bf428e7a06`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:58:46 GMT
SHELL [cmd /S /C]
# Thu, 11 Jan 2024 00:58:47 GMT
USER ContainerAdministrator
# Thu, 11 Jan 2024 00:58:49 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 11 Jan 2024 00:58:49 GMT
USER ContainerUser
# Thu, 11 Jan 2024 00:58:51 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Thu, 11 Jan 2024 00:58:51 GMT
ENV MONGO_VERSION=6.0.12
# Thu, 11 Jan 2024 00:59:25 GMT
COPY dir:329dc1f21a61007915141205ec19b27dc3ea273dd304d374db84e0d8d0974daa in C:\mongodb 
# Thu, 11 Jan 2024 00:59:30 GMT
RUN mongod --version
# Thu, 11 Jan 2024 00:59:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jan 2024 00:59:31 GMT
EXPOSE 27017
# Thu, 11 Jan 2024 00:59:32 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763adc5d4f572b44687748267a9806c81f129e60f725e979319d332d4e7b01f6`  
		Last Modified: Thu, 11 Jan 2024 00:59:37 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73143e2dffe0a96e3b13dc2c6bd1548ef6e9d491127195b3b1f5713964d037d7`  
		Last Modified: Thu, 11 Jan 2024 00:59:36 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075043674cfde3dfa29d839507c4c0a960d0a704ca3d5ee6b7d12aad9d1cb4a8`  
		Last Modified: Thu, 11 Jan 2024 00:59:35 GMT  
		Size: 69.0 KB (69034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65a7e01c8f1d71e2ec35f2c0fa359e80c6b73608255c40058710ac92d32863e`  
		Last Modified: Thu, 11 Jan 2024 00:59:35 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318acd71f8adeba00c61e681bac59ca990af4250cf643c4eeff5de294f9a6155`  
		Last Modified: Thu, 11 Jan 2024 00:59:35 GMT  
		Size: 267.1 KB (267055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf2a2a3882229f6d07dbd1ef8759253f67d0feb8769c12f0163976223cd45f3`  
		Last Modified: Thu, 11 Jan 2024 00:59:35 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0e194c63daa9d14487e48c039b64a9f733b5026069f7506114f388174d982c`  
		Last Modified: Thu, 11 Jan 2024 01:00:20 GMT  
		Size: 517.4 MB (517399559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7755d3500b88e864da4ac4b27bfe12f8f12ebf65b70b0d6095dbf7e47859f7c`  
		Last Modified: Thu, 11 Jan 2024 00:59:34 GMT  
		Size: 71.1 KB (71096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18845d9a5d1c57deba8a8d8992737251ea9d74d1d7317ce33dbe9ff477be5b62`  
		Last Modified: Thu, 11 Jan 2024 00:59:34 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84623cca30ceaec325b1b075d338815008d816ba0eeabc22f69aeaad26260bc`  
		Last Modified: Thu, 11 Jan 2024 00:59:34 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc3ef7889ce223007ee3817c82208c6c36e9623512c3e5e460f4afadcd3a8e6`  
		Last Modified: Thu, 11 Jan 2024 00:59:34 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
