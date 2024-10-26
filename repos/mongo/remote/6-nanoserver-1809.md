## `mongo:6-nanoserver-1809`

```console
$ docker pull mongo@sha256:9849fc3c8a87d6330c83bf95198d3e6a7d821fad2aeefcb3c39822cef361aa9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `mongo:6-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull mongo@sha256:016a76818cc466558e6eb53c38850c8f96a32db18da382a1835d3a9a10e49c7f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.2 MB (681195335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0947f595b10d918173aa0a3e5e48dc8e76c1665f8fbe5ca5d65b516b821f969`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Sat, 26 Oct 2024 01:49:33 GMT
SHELL [cmd /S /C]
# Sat, 26 Oct 2024 01:49:35 GMT
USER ContainerAdministrator
# Sat, 26 Oct 2024 01:49:48 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 26 Oct 2024 01:49:49 GMT
USER ContainerUser
# Sat, 26 Oct 2024 01:49:52 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Sat, 26 Oct 2024 01:49:53 GMT
ENV MONGO_VERSION=6.0.19
# Sat, 26 Oct 2024 01:50:25 GMT
COPY dir:f97029ff7a52e12f6b8e5522b58ebccd35083615a35a3126b84db5898f526c7b in C:\mongodb 
# Sat, 26 Oct 2024 01:50:35 GMT
RUN mongod --version
# Sat, 26 Oct 2024 01:50:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 26 Oct 2024 01:50:36 GMT
EXPOSE 27017
# Sat, 26 Oct 2024 01:50:37 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1738fdf8dc0c020002cbdd16275ba7bd14f5cd265356d7af6e0455f5e5e08ddd`  
		Last Modified: Sat, 26 Oct 2024 01:50:41 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87da13a0b58a28567dc3916bc9c9ad53bd235c24df3f1ada6f87f0b9db3c666`  
		Last Modified: Sat, 26 Oct 2024 01:50:41 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81dbc65beef011ee9d23b02974a02c585a699cb362eacc12c23bfe8c3da230c`  
		Last Modified: Sat, 26 Oct 2024 01:50:41 GMT  
		Size: 66.4 KB (66379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6d4cbe4fadfdd610488f61a53963c4cf6bf9464f9ab2f19c26e0793cb4c78a`  
		Last Modified: Sat, 26 Oct 2024 01:50:40 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be82cc0aff086ca22f497457919f2276d888990865f6113bb93b899e1b446cb`  
		Last Modified: Sat, 26 Oct 2024 01:50:40 GMT  
		Size: 275.2 KB (275171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402af1348c34168a15169a867920c5673840794058f7cd18850bea40be551f1a`  
		Last Modified: Sat, 26 Oct 2024 01:50:40 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886252777bb069fb083e7239f66542744ef70f730812ffb2ac94b1f5d8512857`  
		Last Modified: Sat, 26 Oct 2024 01:51:22 GMT  
		Size: 525.7 MB (525677137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56353fa33f3efdcab83f1e549e82a1b7eb2c4baaf72c35917082ae53e52ecb8`  
		Last Modified: Sat, 26 Oct 2024 01:50:39 GMT  
		Size: 75.8 KB (75771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cacf40ada7b6d6fdd3854d5c2e0516d8c7ac62c6cd1da8611e1b976231fae2`  
		Last Modified: Sat, 26 Oct 2024 01:50:39 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33456f29ddac4f2ceb457e2e4469336a419fb012e4a91d6d44665c2ecc95c4e`  
		Last Modified: Sat, 26 Oct 2024 01:50:39 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3610795dfdab7740a5718c46622dff280de12e847a8844ed941b1f2bc78765eb`  
		Last Modified: Sat, 26 Oct 2024 01:50:39 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
