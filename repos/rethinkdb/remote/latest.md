## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:914c61d22875d025fc5954f0383c881214b39e746f6b29eb23d1cafbd0dc4422
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:66ba19eb337f0f83c71e1d7dea90016fe5df6550ebeb0305f7c1f5031de77b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47991593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94bba551b7a8ce680db4dead5011225c0d19ab51b7fa9d631deab38a80b1b64`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a3f9cbb258098351b58bd49faf57e28c1dfccd6e436ba40e0ee0c6cd376456`  
		Last Modified: Mon, 17 Mar 2025 23:13:24 GMT  
		Size: 9.8 MB (9791288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfa46c6149b73adbe19d819c8e6d31fa08ee7948d9790409669464661583cd4`  
		Last Modified: Mon, 17 Mar 2025 23:13:23 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490002b7ae303e52265bf00c204393211823d38a7b8f5b2b82811181605bb799`  
		Last Modified: Mon, 17 Mar 2025 23:13:24 GMT  
		Size: 10.0 MB (9992679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1321bcd1c86c9220412ba116a8ff6e99eda7ad873d46fa9ec9cec19c1a8b0c`  
		Last Modified: Mon, 17 Mar 2025 23:13:23 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:e703082797a434ac4319e23967c8389d09cb840c9f2036e69c8691992e95233c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179c1f297530c43cc93a9bbef38c0a5405bbd96e131a511aa8a0d11eff2a67f1`

```dockerfile
```

-	Layers:
	-	`sha256:8d6b01d1c195d95db26dfa503860f2df2d08bca52a67fe454a13e7f2831f6ec7`  
		Last Modified: Mon, 17 Mar 2025 23:13:23 GMT  
		Size: 2.6 MB (2626155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39101fdd69f941052f2a682c5e0a3218a7c97d62399cb5d397ed35d2bd4dcf64`  
		Last Modified: Mon, 17 Mar 2025 23:13:23 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:f78aa071f0d1986784d0734e4f6aca187b01f9bdddc529f7663effb475a87bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47002363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bddd5094e9eefbf9cefa6d94224b923858c5684c9f905a91f27de1904510c3ed`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5d165c25d7451c9dcf07a9ed0aebab022a0d75f8f8f81e94343e5dd79478c7`  
		Last Modified: Tue, 25 Feb 2025 05:20:07 GMT  
		Size: 9.6 MB (9588703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418aafa3fab2f0e02e2cf945212d3c04e3117174e2da17f27ef726e4bb06a449`  
		Last Modified: Tue, 25 Feb 2025 05:20:06 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eaaf95cee9126f51ab7f648ebb1f79df3efed41b9b1ec2ac66ca18ec9f7d17`  
		Last Modified: Tue, 25 Feb 2025 05:20:07 GMT  
		Size: 9.4 MB (9362472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7fd8d22a6e8a3606b1c185d1ea70744561f9009f9c1ff6700ec423979ef43b`  
		Last Modified: Tue, 25 Feb 2025 05:20:07 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c8df483d3a69359595d9724c103c51c63fc9c658d6cdbf942f8c4218bab60b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65163324ed50f22237a0c96005e6674d10004925bf5bffe9383ceea27d15868f`

```dockerfile
```

-	Layers:
	-	`sha256:a0a8cb0c84f1577669c5e4900ce368763752d40ac3247c268156920c4ce1a8fe`  
		Last Modified: Tue, 25 Feb 2025 05:20:07 GMT  
		Size: 2.6 MB (2626478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:127c182f093bcfa82d3a87faac1dcf614dc94fe9704ddb6a5c555ea1f66cfd06`  
		Last Modified: Tue, 25 Feb 2025 05:20:07 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:1f5cb3620207881b1a0b8e7109bf123d5ef76d58eeda0d892fa9a3655280e277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45457157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d34dba56937ff17e551ea0f1045b257a9f51d9ab8092f7b347ccc34636e365`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036217152bd928008d4402ef366563a7c358fd59e04ffa3d6dc39b9b838d0bb5`  
		Last Modified: Tue, 18 Mar 2025 03:07:07 GMT  
		Size: 9.3 MB (9289816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8766fa9ffb794adf597344d861f0168ccfdba452d1a33342ef654cd98fc2234`  
		Last Modified: Tue, 18 Mar 2025 03:07:06 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2353cf34436d8dcb68704523e733abe03b6f191ddf133b836b7071be9ae54d42`  
		Last Modified: Tue, 18 Mar 2025 03:07:07 GMT  
		Size: 9.3 MB (9303520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fca5e0faad4b05778ed939a2c69484f0ea784a781a407a1fa8f9443102b8ae`  
		Last Modified: Tue, 18 Mar 2025 03:07:06 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:b2ca0b1a7f2f593a8856da77e3ff717c8e77ec25afe7e418438ddc1ec47e65aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6735b6ee180cbd1bcaf7a86a5be6c7c85ec2e437a15d826b13edc7196dad7eda`

```dockerfile
```

-	Layers:
	-	`sha256:089ca4d432cdee7fd8aafcbd764efb015ef8abefe13d328b5f4fd4dce30c21d7`  
		Last Modified: Tue, 18 Mar 2025 03:07:07 GMT  
		Size: 2.6 MB (2625249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b887f638f141fa2ab53074fc3c47bee8348b7cc18fd38240636659bbb7f774a`  
		Last Modified: Tue, 18 Mar 2025 03:07:06 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
