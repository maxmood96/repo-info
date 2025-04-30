## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:af4b76ecd1d68cdc63c7180de728e23670044b67054f14fca713485b83f39485
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5c90b2c936d2cdb4c732b2ba7b5aaebe5625c9a7fe24644f2da7db61155b529d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143964253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fedf5c0537e37929a8505fde389edb2fb2d4b2c32dc9cbd58d46af043aab2b6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6907e7a95a9eb9260700c6794ec9f337aaefea96179dda4d1e82835f67ea05b6`  
		Last Modified: Mon, 28 Apr 2025 22:06:16 GMT  
		Size: 54.7 MB (54716148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367fdbaa928c8eae0b7fc7d481505880642616ff2a4885e784e2c638777f06a4`  
		Last Modified: Mon, 28 Apr 2025 22:06:16 GMT  
		Size: 59.0 MB (58992858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4ca7476658877c77848188c93aaca822e6063adc72d201e2593a174ecbd49`  
		Last Modified: Mon, 28 Apr 2025 22:06:14 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec9a812bf6ef2422e5687638b970a47b831cea755f106af808f7e124e813a721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf08042bc0d220840081d78570ac6e160f94a16f0a05b55d92fb76356d37a2e`

```dockerfile
```

-	Layers:
	-	`sha256:c3107a378f4eee84b6f6e859b0eb7d4456f10dace9633ac4a1c4ab13c0f679b8`  
		Last Modified: Mon, 28 Apr 2025 22:06:14 GMT  
		Size: 5.2 MB (5240677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6494e97153f10c50bab1aa40cc785795b63b345cd98a00c170c7becc3430db46`  
		Last Modified: Mon, 28 Apr 2025 22:06:14 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:921b96c52ec7168ed42522fd9fc664cc89fc11c1a455c5d532ed877209bb2c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141703192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dc443022b1f88c0c80f03719a0998507886ff2d2cc93166ba0aee58176ead6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9362c53d1c14ecfefba9cf38dd0fa524f1f96fc993f360367b03a91b556103f`  
		Last Modified: Wed, 30 Apr 2025 01:00:56 GMT  
		Size: 53.8 MB (53830503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8d67647b92f1f5f5dd98c61327d4113d300f34a9f4dd2555843c503eb3aae9`  
		Last Modified: Wed, 30 Apr 2025 01:03:37 GMT  
		Size: 59.1 MB (59127402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc57bf9dc32ce128463041f93704e685c08353465d76eb509d6c9eee0daa51bc`  
		Last Modified: Wed, 30 Apr 2025 01:03:35 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b383d44a76fd35cdff11028d68801824d2fff0ffb70e0500632d26a1fc4a9dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5261516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445065c8a8455f482908e4f3eaf183d8dc9dbece76e4b400f5e2ecf3cc625d0a`

```dockerfile
```

-	Layers:
	-	`sha256:01c6844cc0412a9c701804096738c15b4e902b757bc9eba70e1d628974b5d399`  
		Last Modified: Wed, 30 Apr 2025 01:03:36 GMT  
		Size: 5.2 MB (5247107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa1dd75484a67b0fe96de92bc2ae58972685e703a15f81179ce17a7c4cc83a21`  
		Last Modified: Wed, 30 Apr 2025 01:03:35 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
