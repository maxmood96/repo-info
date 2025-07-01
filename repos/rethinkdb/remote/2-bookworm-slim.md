## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:42997973c218db6ce67c363275eef4bfac98fa0c26c914fb9627c36b611e24cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:c02994a66debb9c42204ce5e6ceb15687a597ffffe773cf12f02a2a88ec20f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48020761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965be68736528e41f7e3fb1e03869be919337ad0f53531b42f2d37d0c786c7cb`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfab3a5b4090702540debf3b3b5167a6a61071d9f00d104ff5d6d9726b011b21`  
		Last Modified: Tue, 01 Jul 2025 02:24:59 GMT  
		Size: 9.8 MB (9795011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e844dfe49d4a0fcf03ff6db31b7d171defd1e014568ea353a576db122040abf9`  
		Last Modified: Tue, 01 Jul 2025 02:24:58 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d19b361d71c49fff9b3863fa889abebb7211d49e356b67eaec7a600eba43799`  
		Last Modified: Tue, 01 Jul 2025 02:24:59 GMT  
		Size: 10.0 MB (9992847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97be8f25ae604c8ae013c763497b5306775064d05b6d92f9108e6b5a18779ba`  
		Last Modified: Tue, 01 Jul 2025 02:24:58 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:027e89c7987aa760c3acfbc4f6829c74a7404a70b7998a56ccd5d25a6b2cd88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2796188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d4a78492a88d97ce62622b7ba410b1518d7f067036933f331d7b4b7c73e02b`

```dockerfile
```

-	Layers:
	-	`sha256:21b1668d8a7ef461f47201d9e2adfd85cde303d541006e1ba43bf3f58ae98107`  
		Last Modified: Tue, 01 Jul 2025 04:03:17 GMT  
		Size: 2.8 MB (2782741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0628af1da5dec632611749147921288755d8223591193e4f9516f7d37f6d944f`  
		Last Modified: Tue, 01 Jul 2025 04:03:18 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:63773da3fb8f4ceb8b9ecff0e2635b5b97f4c767e65c845adb11e3166978c822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47034280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6844e3972192e6c396448b51a534f138e6b7952967205f3240679bac038335`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e842d3928ae192699d24090a12d956c1d9d0d11d34d3189278da85e596be6d47`  
		Last Modified: Tue, 01 Jul 2025 06:32:08 GMT  
		Size: 9.6 MB (9591265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583958ea8965a848dba16abdd70b607dc63f27e46ae8fe3911bc9fea794349c5`  
		Last Modified: Tue, 01 Jul 2025 06:32:06 GMT  
		Size: 2.7 KB (2671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a10c2407cebafaad6e8b92fb956457b1304393265b83f0c58f5e4f1a1b3c6d`  
		Last Modified: Tue, 01 Jul 2025 06:32:07 GMT  
		Size: 9.4 MB (9362574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c0b6b81b342eb63290b82ae6d935905a9246479f45c3cac1cdf4ff8377903f`  
		Last Modified: Tue, 01 Jul 2025 06:32:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:5ad043bd09e1b04de5eb8dbed4362fe2900c76f14cd6a0d658a456d589a69ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2796705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fb6d39d7bb8d875d277dcb2190f9c9aab9136972306cc809f302dfde00041d`

```dockerfile
```

-	Layers:
	-	`sha256:4e67bbb5bedede9db1459e98cb0136156c964baba342647a4abe7f385dc02d0c`  
		Last Modified: Tue, 01 Jul 2025 10:05:54 GMT  
		Size: 2.8 MB (2783076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0526bfae0ae43bea2ee69496d84cb751bb723b5fd1f2376cc9b91447b7cee3`  
		Last Modified: Tue, 01 Jul 2025 10:05:55 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:09e40e75dea04aa229df4e2cdecf9fbed834d2c496c66f999a6fabb4aeaead9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45489001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9c6ba5ec052281b30b93a3d05aba682b3743802bcc33020321a2f3a209c6f8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5847fb9b069f59d4ce66168c1f54a4dbe670f73d4331e65574cca7882cdd2b9f`  
		Last Modified: Tue, 01 Jul 2025 07:15:15 GMT  
		Size: 9.3 MB (9294841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edfadc81db7c966fef3b3dacd9eb5b5608b34be6c5e672d8971392ded9fb49a`  
		Last Modified: Tue, 01 Jul 2025 05:28:02 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8007b984f94fc3235b760d53481eacd6f88bb75e4d91b80d7503797cfc28b9f3`  
		Last Modified: Tue, 01 Jul 2025 07:15:18 GMT  
		Size: 9.3 MB (9303589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3d8383d8c1fe16615fb5f5801725d71b4688e1c7494ada35f30109d15e6b4d`  
		Last Modified: Tue, 01 Jul 2025 05:28:04 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:6acf490a8c9915f859f4a13f5ff3ba288db467275aef468929bbbce683181da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2792390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26414e8b813ef16b7ec710ad362f38fdf09a45825e97b8623da1f0fe167b4f6b`

```dockerfile
```

-	Layers:
	-	`sha256:16de27150723681cc73cbca893fdff2c0a92c4d18504925b3e17878c9934fead`  
		Last Modified: Tue, 01 Jul 2025 07:03:24 GMT  
		Size: 2.8 MB (2778943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56376b28eae1e4eecb292572ca2a98d173f4b35a0cb232562790b7161136ef1`  
		Last Modified: Tue, 01 Jul 2025 07:03:25 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
