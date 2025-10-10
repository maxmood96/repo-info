## `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:4f84d2e6aab6ccaf36553a5742c484322feddf8f4fd195b2ee815f01955af371
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye` - linux; amd64

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

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1178e618716021bf9de054d209faecfd5b0768f6dc3cb3b3c18d105e5f58710b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278027210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e59b8d754f521d2fac363de1698911bf0665b5c7069a3129cb2cc05cd5c252`
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
	-	`sha256:767592263961742e8218b9f8450fb07a850804cdcb5cdda70ad3e7e9c7e5cec4`  
		Last Modified: Sun, 05 Oct 2025 09:22:09 GMT  
		Size: 156.1 MB (156081248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d10676b63f5e642ee1e418879cba0e191f6a15c863562f25f2683985f317319`  
		Last Modified: Thu, 02 Oct 2025 02:46:01 GMT  
		Size: 69.7 MB (69687505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbaa1d06709e090a4c9d01cdc1475b9e83333d1ed314fa8d321da249ea6455b`  
		Last Modified: Thu, 02 Oct 2025 02:45:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3cf550109a64eebc2feada676a09549233a406d2ba870cb11fc7a67bc7ab25`  
		Last Modified: Thu, 02 Oct 2025 02:45:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:046c85c43d5c122aafe880acaa3bbea75cbad21ee7107cb939c2081b644db2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9ef7edd35bb1fa22b53370588354fe694a34e6760aaad3fe023267bb4a690a`

```dockerfile
```

-	Layers:
	-	`sha256:be9adef91ac4afd4edf72a30c6ed7b75a8e409baae0b3e7e8cabb3a727d4eaf8`  
		Last Modified: Thu, 02 Oct 2025 06:42:45 GMT  
		Size: 7.4 MB (7403868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a19c25f9177f1656891a2f06df9d1eddfdb620c27f65b7a1b28d7fec67546e`  
		Last Modified: Thu, 02 Oct 2025 06:42:46 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
