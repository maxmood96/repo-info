## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:b1e9c040ad4e314a30178d119a88e209f88b8f34f9b7d6ea875f74e1f0f2f95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull mongo@sha256:cb72883aad27d2826285d483cc10e68d91e754ff940f6b00cc4a253c7ecf6261
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.0 MB (715003193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7093839a43120ec2b06d2f5e4056253443707f8979b6afeb269d4c2516d1c2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 02:31:25 GMT
SHELL [cmd /S /C]
# Wed, 11 Oct 2023 03:06:25 GMT
USER ContainerAdministrator
# Wed, 11 Oct 2023 03:06:58 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 Oct 2023 03:06:59 GMT
USER ContainerUser
# Wed, 11 Oct 2023 03:07:00 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 11 Oct 2023 03:07:01 GMT
ENV MONGO_VERSION=7.0.2
# Wed, 11 Oct 2023 03:07:59 GMT
COPY dir:966ad16c981f6f8ba3ff3658fdecd39e439aaa39e251615778ccd8944fcbfd3e in C:\mongodb 
# Wed, 11 Oct 2023 03:08:24 GMT
RUN mongod --version
# Wed, 11 Oct 2023 03:08:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Oct 2023 03:08:25 GMT
EXPOSE 27017
# Wed, 11 Oct 2023 03:08:26 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1d090bf86f6024502bc8f94ffdf6082818dc40adde892065acecc65617301f`  
		Last Modified: Wed, 11 Oct 2023 02:48:49 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884f2cb9b5edcbbf4b0b83f11a2ca9e93da04c86243865ff1f331445db9abcf3`  
		Last Modified: Wed, 11 Oct 2023 07:43:05 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7c6a1f7c9281c4d2be3cef0ad78603721509d8a2a8f6bc3411192f8112c273`  
		Last Modified: Wed, 11 Oct 2023 07:43:04 GMT  
		Size: 69.0 KB (69002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3529e287318b8e986a6ed2518bcd876b733f1577a5c44c2528bbc77778272a`  
		Last Modified: Wed, 11 Oct 2023 07:43:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7282f0ce93e521c5382bb7a008ed67429bd97f092d002c5cbcda26eb63e6708`  
		Last Modified: Wed, 11 Oct 2023 07:43:04 GMT  
		Size: 267.2 KB (267195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a7f551953b3d3224a67ac606b71722efe631ce988df63a0249b7aa5a0e3bd9`  
		Last Modified: Wed, 11 Oct 2023 07:43:03 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e59f759eed1256ec46ffb0627b2b0153ab9fc9e373274d48ea3066051399c9`  
		Last Modified: Wed, 11 Oct 2023 07:44:19 GMT  
		Size: 610.1 MB (610111594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777baa881aaa37d7f1cf992ff1008278d584adba5f0edbf6873d37ba4aecdc17`  
		Last Modified: Wed, 11 Oct 2023 07:43:02 GMT  
		Size: 82.7 KB (82716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e838112e2030a362b79e9667aea24f5b1c7e45914daf16bc0943b0bb177842`  
		Last Modified: Wed, 11 Oct 2023 07:43:01 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ecd44391918c062dc98d337890a587f8b4ef3e3cc0c55be2f2855da49df88f`  
		Last Modified: Wed, 11 Oct 2023 07:43:01 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d040c29596876b59bf8ddcd9c76f74e66d4a8be8f4a9871a024cc22036a3e1`  
		Last Modified: Wed, 11 Oct 2023 07:43:01 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
