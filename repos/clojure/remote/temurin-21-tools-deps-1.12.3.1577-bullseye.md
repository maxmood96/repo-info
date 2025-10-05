## `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:38cba206dcfe74a0a111c95eccf3ae6bc3541c9d3dba6154f6fa5c4d4c0b5213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:85f470dbea5605d25410860845f4855a1b44e53f4a278829e7027ed68c4351e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281121662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a9f2933d356e91aa67bedd68c07841058a3b816ba1186d17e2e12bb32daca2`
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
	-	`sha256:5e9895e3c05361863dff0235e5468d09668763cb297fb9c1559dcc67d68599fc`  
		Last Modified: Thu, 02 Oct 2025 20:37:54 GMT  
		Size: 157.8 MB (157804827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49086acb9e71a84b3a3ce0d6591b068c1df76a581ce3fb1b54324f6aefad150`  
		Last Modified: Thu, 02 Oct 2025 09:00:30 GMT  
		Size: 69.6 MB (69559728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe04b5d9577b4712a0ed5cd6684f70f970a7dc6f9c3fa32f988d22b674581a1c`  
		Last Modified: Thu, 02 Oct 2025 09:00:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbe6fd6472b6bd75b8279b54034559fafb490330bb10f62777852ed61aa22de`  
		Last Modified: Thu, 02 Oct 2025 09:00:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0c474a6bf7ee072e0366349763e878867b8458d9f5f9b620fec7d5e8b55f5d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9c59984f147cfb375f4989a3cee1d931da145f05a37b58dfdc27305c4f64fd`

```dockerfile
```

-	Layers:
	-	`sha256:551452b1aad748ac32245375f05102b42dd857e8847f26b8ebfae9852951d8bb`  
		Last Modified: Thu, 02 Oct 2025 12:40:47 GMT  
		Size: 7.4 MB (7398769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a898d6eed8d4d930ed94c0a81f9b0c66e6a91611bd4d7033845dd112e4b1ce5e`  
		Last Modified: Thu, 02 Oct 2025 12:40:48 GMT  
		Size: 15.8 KB (15820 bytes)  
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
