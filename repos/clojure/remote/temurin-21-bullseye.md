## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:ba107e7ec1b22d9c1ed48d408ae34297a79105ff43c883cdb31effdb4df56f45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7e9a47e00e533a2399c51dec1c0df1a5f45bf1c3a7ad0e33bc54138cf785b5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281122733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b38a3649ec3a7cf236f97a961aae513c3630bc57f0e0d1f865fad6674e82d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454384ce4e88b86752048338e00df9cb0a36f7dce288df661a8b6e58e0289992`  
		Last Modified: Thu, 09 Oct 2025 22:29:49 GMT  
		Size: 157.8 MB (157804769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5628505f65b0ce319cbe31ef446757811a2bf6c4ef3b9f6813d02dc5ecd9412a`  
		Last Modified: Thu, 09 Oct 2025 22:30:14 GMT  
		Size: 69.6 MB (69560856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefdec1a7c3662e0b4a4b86e420745c7a0b4dbfe8b7b8d170aa2b58f4f4542c0`  
		Last Modified: Thu, 09 Oct 2025 22:30:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4b12c6ccd1d89ed8249c98ebe99e95a947424f7baca08bed814712c75426ac`  
		Last Modified: Thu, 09 Oct 2025 22:30:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:be9bb4ba154873abe96e48929712051ae9e8185694c2de62f98a338911cc47ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6779b35d5378495365c824916c7dea4f8a8dd32a3e2f096b953d195676c530ff`

```dockerfile
```

-	Layers:
	-	`sha256:356873eeb153bd88b3bd9ea06838eec726eb6a15299f5aae5f810f870f9f3bb0`  
		Last Modified: Fri, 10 Oct 2025 03:36:16 GMT  
		Size: 7.4 MB (7400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce12aab49e8935b34aae28aeaee1834188950ffd2b65c099d25f2a7eadbcd1eb`  
		Last Modified: Fri, 10 Oct 2025 03:36:17 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:536205fd81a1c3c2a4572af0e7b895d84387468d267568f26d84564c78db9551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278027813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaafb57d900ac72ad95d1d4151d6276197866e315b761a569c22acbe7dcdd4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f77dac182b1a96d9c57755b94674ac0e92a179095c7d1153368b235fbd4e159`  
		Last Modified: Thu, 09 Oct 2025 22:29:47 GMT  
		Size: 156.1 MB (156081239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70621075cf2c38a6b41986b8947a5aa6d800c356d392362d8b5719b0820adb8`  
		Last Modified: Thu, 09 Oct 2025 22:30:09 GMT  
		Size: 69.7 MB (69688120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcd135985b318fcc6de821c5f165df2f0775dbc4f68177b9e663afb49eee9df`  
		Last Modified: Thu, 09 Oct 2025 22:30:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a517cb40ad4b0664800f5a74868c1e1799acdec6317812032c0905db094203c`  
		Last Modified: Thu, 09 Oct 2025 22:30:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:53028e678ca8e87517cd1dbe93a64825b07f26721a633be046e3082430ab21f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2459a687ee0346fc556fd9320a54157e3dbdd86f1a97964a2c3f9a3710a8a0cd`

```dockerfile
```

-	Layers:
	-	`sha256:8773f6b51014f73ff81fbe4ea02941306e05e32f1e86ef5c054402a5e29c5cbc`  
		Last Modified: Fri, 10 Oct 2025 06:43:43 GMT  
		Size: 7.4 MB (7405492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3fa478656e0479fc01d39219132b3f01a08fe8207e9138a06024c451cb3c005`  
		Last Modified: Fri, 10 Oct 2025 06:43:44 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
