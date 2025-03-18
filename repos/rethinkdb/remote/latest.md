## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:45935d6925795e4b3153888f4297aaf2f09ffe43a06a943a8f5b99ec1a9693ce
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
$ docker pull rethinkdb@sha256:b3c3be4b43b69af3159412094e671143619496500fbbb839f90cbc18dd4fa114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46998215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb6f1866d2d1244c3d4025f16ef325c33d72f602697d1bfa50a7a0ffc4f71c6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84ed1a87db46ba63a0978f10490d87515ed391d9e4c7a07c2a0d9b20ec4394c`  
		Last Modified: Tue, 18 Mar 2025 06:27:24 GMT  
		Size: 9.6 MB (9588902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc470f63ce975f45137610a95df7f03889bb2d51a59b926b3b53304da58dd7c`  
		Last Modified: Tue, 18 Mar 2025 06:27:24 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7576a12064b00820e6521e69d7b3eb9531cb888cf23bdb5e196c632695f7571`  
		Last Modified: Tue, 18 Mar 2025 06:27:24 GMT  
		Size: 9.4 MB (9362514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7e6b4aa33cced7c460b8343f7dcb572542d4ca26f2a44cf9cfa3393c371861`  
		Last Modified: Tue, 18 Mar 2025 06:27:24 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:5b2e0ab18707f769ec8f8f8214fd2c3fe4c445c5a0bb71c2bb8fe2d599a2a18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6db2590e62b7460df33f6e51b160181199307787b9e3e0c20b0c458562fd28`

```dockerfile
```

-	Layers:
	-	`sha256:525450912e615c93dcad8947e0b37325cb978f5d7dd225e2fc88a68d449376a4`  
		Last Modified: Tue, 18 Mar 2025 06:27:24 GMT  
		Size: 2.6 MB (2626490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01e10eeeaf129af70c40d7147736615c3e52ca8409ff46cc92738f5f67e111c9`  
		Last Modified: Tue, 18 Mar 2025 06:27:24 GMT  
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
