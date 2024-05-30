## `mongo:7-nanoserver-1809`

```console
$ docker pull mongo@sha256:f16cb0042909feb7ab9000dda3e7ccaacf02f25f13daf784a4225c36bee22746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `mongo:7-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull mongo@sha256:f458cda336850716230d85838e57ccd925bba0e857a05a16cd042df77011302c
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **773.5 MB (773523955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bd87355a5105feddc990a5fc51cb8c2577af25f59f421836e0426bd6f4064c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 29 May 2024 23:02:08 GMT
SHELL [cmd /S /C]
# Wed, 29 May 2024 23:02:10 GMT
USER ContainerAdministrator
# Wed, 29 May 2024 23:02:27 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 29 May 2024 23:02:28 GMT
USER ContainerUser
# Wed, 29 May 2024 23:02:33 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 29 May 2024 23:02:34 GMT
ENV MONGO_VERSION=7.0.11
# Wed, 29 May 2024 23:03:20 GMT
COPY dir:19a9c5e7b92e67df364a58952a43fa9635a4cea236c07894dad5b3a27bc56ae4 in C:\mongodb 
# Wed, 29 May 2024 23:03:35 GMT
RUN mongod --version
# Wed, 29 May 2024 23:03:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 29 May 2024 23:03:36 GMT
EXPOSE 27017
# Wed, 29 May 2024 23:03:37 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70747260debc2c7f06b863a7f595131b2a1b226e9e2c1266057c5338edb2268a`  
		Last Modified: Wed, 29 May 2024 23:03:45 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6ce8306fb3aada8f9c39d69acc7f71ce8c6d658d92e38b861a0c69b15aaf4b`  
		Last Modified: Wed, 29 May 2024 23:03:45 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d309f8f2d63598e88136cf1fe61f380f90919d6df5e5563f64492f4d92595db2`  
		Last Modified: Wed, 29 May 2024 23:03:44 GMT  
		Size: 68.1 KB (68052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044474cab89849a1d724ce992b5ba990f2222fc4287ffa2766cd9c09fc8925cd`  
		Last Modified: Wed, 29 May 2024 23:03:43 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500501c77de94bbc7bec2a89645790afb3f4ae2ed4cb740db544182bcc528fce`  
		Last Modified: Wed, 29 May 2024 23:03:43 GMT  
		Size: 267.1 KB (267078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f448f94451a3504e65cdefff72b31a4386cd7985b50d7898a81c56eb956441c6`  
		Last Modified: Wed, 29 May 2024 23:03:43 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3a50598ae731b3829f8755ee07d491ee3fb000fe5b078312b61b1859e20999`  
		Last Modified: Wed, 29 May 2024 23:04:32 GMT  
		Size: 618.2 MB (618172287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccb8f1239194b2834dd6edb651205be5c9d614576645f78119dce23441b5c75`  
		Last Modified: Wed, 29 May 2024 23:03:42 GMT  
		Size: 67.9 KB (67923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca608e478a340264743b2ddececc43b846e209637600021618e350c58f42883`  
		Last Modified: Wed, 29 May 2024 23:03:41 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d12a761d047c34757ec3f036f8de5e05197f1fe9c7e68b9099a5b1d1af4eb39`  
		Last Modified: Wed, 29 May 2024 23:03:41 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbee5a1388216cfb9e1673cc7219fad5b9a93864e53aebf0fea74a5b9b68bf19`  
		Last Modified: Wed, 29 May 2024 23:03:41 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
