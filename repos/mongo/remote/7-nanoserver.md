## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:b02df04028acd38d9f220a61b20864eff44d130471a63a99ece3e08f67ac7c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.4773; amd64

```console
$ docker pull mongo@sha256:b8a4e777e8ae257416355a2698b5fc45fea7ae62058d28cec3e6b8ebbbe4cd83
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **745.5 MB (745520875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719f47c0e983af29c3b003146d1a9fa5b0021fa250904bda09c4d789a0909b54`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 00:15:18 GMT
SHELL [cmd /S /C]
# Wed, 11 Feb 2026 00:15:18 GMT
USER ContainerAdministrator
# Wed, 11 Feb 2026 00:15:24 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 Feb 2026 00:15:24 GMT
USER ContainerUser
# Wed, 11 Feb 2026 00:15:26 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Wed, 11 Feb 2026 00:15:27 GMT
ENV MONGO_VERSION=7.0.30
# Wed, 11 Feb 2026 00:16:00 GMT
COPY dir:8685c746c7b2037d5dacae29a39bd4a50f54de3d48c0ef6fdff51ad7f000e5b7 in C:\mongodb 
# Wed, 11 Feb 2026 00:16:17 GMT
RUN mongod --version
# Wed, 11 Feb 2026 00:16:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Feb 2026 00:16:18 GMT
EXPOSE 27017
# Wed, 11 Feb 2026 00:16:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830de5d93459ffa3d6047bbe5564982c9088a109e6e2025f23d9f9b2b464626c`  
		Last Modified: Wed, 11 Feb 2026 00:16:30 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acda0d0986bd3d889dbfa5300e5d59136aaaabefca4e45195101c5134273216`  
		Last Modified: Wed, 11 Feb 2026 00:16:30 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0260afac996e398edcdb6c29edcd83103dc791d3b84e745496e1193ccdad5dd4`  
		Last Modified: Wed, 11 Feb 2026 00:16:29 GMT  
		Size: 73.4 KB (73424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc54f30be2f197fc457140e6b5d825d90c225836003193bf9ac1ce548b71b3cb`  
		Last Modified: Wed, 11 Feb 2026 00:16:29 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334e926698393fc73b1947bd5232c3b0c56d8890a7a7a9faea33427b41543667`  
		Last Modified: Wed, 11 Feb 2026 00:16:29 GMT  
		Size: 275.2 KB (275176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82ac89eb4059673d48637b16a7245a3540ba50155c72aa0e4ec46cee824d619`  
		Last Modified: Wed, 11 Feb 2026 00:16:29 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f85cc6cbbff08a554f343dbecd931ccd56800ca107b4e74e0d1bc5773b5dd`  
		Last Modified: Wed, 11 Feb 2026 00:17:25 GMT  
		Size: 618.4 MB (618433884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4796c1c89f4a049b3a45c1c79c839c2bdf0a8e2481e0587951abccd16240484`  
		Last Modified: Wed, 11 Feb 2026 00:16:27 GMT  
		Size: 85.1 KB (85106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c949e7ee438bcdd688de5e4e09eb7135cae71024375a46cf80ced86d00caea94`  
		Last Modified: Wed, 11 Feb 2026 00:16:27 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd09f46c354308dbb9a7ed827b2219ec4916c129c425de9f212a87c852e56da`  
		Last Modified: Wed, 11 Feb 2026 00:16:27 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea13b0515fe2945f99b886cf12fdc6e75cabe907ebe3b54275b11ae3480c1aeb`  
		Last Modified: Wed, 11 Feb 2026 00:16:27 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
