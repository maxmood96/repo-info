## `mongo:7-nanoserver-1809`

```console
$ docker pull mongo@sha256:015831a9d4605a7118152b68b03563b2460168759fcb6acb0748e347943a81e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `mongo:7-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull mongo@sha256:b1b656278a4b77710d4f416a21582aa509577224ddd885050ab898b5dddcaf18
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.0 MB (763953313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8614514c5b222da27f7019cce996f59760077ab1316b43b82b0ff6e1fd72d510`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Thu, 29 Aug 2024 21:50:29 GMT
SHELL [cmd /S /C]
# Thu, 29 Aug 2024 21:50:33 GMT
USER ContainerAdministrator
# Thu, 29 Aug 2024 21:50:45 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 29 Aug 2024 21:50:45 GMT
USER ContainerUser
# Thu, 29 Aug 2024 21:50:47 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 29 Aug 2024 21:50:48 GMT
ENV MONGO_VERSION=7.0.14
# Thu, 29 Aug 2024 21:51:32 GMT
COPY dir:569dc595e568429f713bfa17916f5a0425b14e2551565b8dcffbac1d9a45d806 in C:\mongodb 
# Thu, 29 Aug 2024 21:51:39 GMT
RUN mongod --version
# Thu, 29 Aug 2024 21:51:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 29 Aug 2024 21:51:40 GMT
EXPOSE 27017
# Thu, 29 Aug 2024 21:51:41 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b492787bf95c7ea32879f0e8498e1cc3aef9853ffbc58f0e66d363ba2642985`  
		Last Modified: Thu, 29 Aug 2024 21:51:48 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ddd4641dc42388a6e84fcf6eded0851661b78e6ea50def1a3778dc44aba957`  
		Last Modified: Thu, 29 Aug 2024 21:51:48 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594bba2b1b8d219f3e89d85bf1eb50599677695a8df05b30262a82759a48407c`  
		Last Modified: Thu, 29 Aug 2024 21:51:46 GMT  
		Size: 67.2 KB (67190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53acbec578bca1a8844627b52d8d75f076d46602698d46bd90696909a9a3393b`  
		Last Modified: Thu, 29 Aug 2024 21:51:46 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1857a420a8fd801d780c482ab7413fdc5cb22bd7daacfc423edef6842d4ff880`  
		Last Modified: Thu, 29 Aug 2024 21:51:46 GMT  
		Size: 275.2 KB (275241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f914db5deba79418096ef2298ec1755c655c29c88eda54a51ca43527aa7eeb5f`  
		Last Modified: Thu, 29 Aug 2024 21:51:46 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd58924f84932af0ad13674828d36261b12c0f18cdc0a355ca003f03f2eb1510`  
		Last Modified: Thu, 29 Aug 2024 21:52:32 GMT  
		Size: 608.5 MB (608452577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c977db69875a3ff20e2a2f952d977ee4a7e0a5ea486cbc3677b53c121b7f66`  
		Last Modified: Thu, 29 Aug 2024 21:51:44 GMT  
		Size: 67.6 KB (67615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f7ea514e5809875863f86b287e1b51d7b5e4007ca3b24a0a1dfee28700ebd0`  
		Last Modified: Thu, 29 Aug 2024 21:51:44 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286be82006c146400be68a95ac13ffdd09472ede0962d96d09799b897e3002f2`  
		Last Modified: Thu, 29 Aug 2024 21:51:44 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97aa2b3fd54870535a2b677aecba23f317b51c841ad02143302d8516960205d9`  
		Last Modified: Thu, 29 Aug 2024 21:51:44 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
