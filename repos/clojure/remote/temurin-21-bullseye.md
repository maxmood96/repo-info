## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:1ad19ce165dd446f8be52ac7a2fcd8b3a98d5efd72e8d3dc195082bb40e452d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0eb2dd7fe55c8ac40aa8b30b60487dd26953a67b79006f0fa83579b8d912f6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281140233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6caf2a7dc3d55706db655e5c7bf3e6247260ce34e94611739e48d4026f92958`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:57:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:57:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:57:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:57:49 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:57:49 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:00:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:00:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:00:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:00:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:00:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48673fd3749e138c2a0c834767f97a421a929bd222295e11f5e3c492deec6ef`  
		Last Modified: Fri, 16 Jan 2026 02:01:24 GMT  
		Size: 157.8 MB (157826001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f94d3b22c738dcb5c934a6cce8ecd51e329e26a72a205408cf09f1eb913bbd`  
		Last Modified: Fri, 16 Jan 2026 02:01:09 GMT  
		Size: 69.6 MB (69556747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56904f71229aac7274d03b5e9c4ac22cee3b4bb299f5d5f5b915aab252a1bc51`  
		Last Modified: Fri, 16 Jan 2026 02:00:58 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be70075b4bca4dc11af742e43712f2772e967daf3301a5a12103a65a2b86067d`  
		Last Modified: Fri, 16 Jan 2026 02:00:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6d1281ddfb373fe7f482345fc57bb3f2af6cdf9e69452f3c537114304ac5568d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291e296fdd1f7db1393fd0c9ff53e2a1d0aef6d207aa54926c90cf6ab5b7739a`

```dockerfile
```

-	Layers:
	-	`sha256:4242dcea64942337d5f270492685279c098a82b49896833066eb6ac8196ded4a`  
		Last Modified: Fri, 16 Jan 2026 02:00:48 GMT  
		Size: 7.4 MB (7398771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08f3a70f675e002e6aa7360be9179dd34ab4d098e8319bfe91f545e64ecc03d0`  
		Last Modified: Fri, 16 Jan 2026 04:45:21 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8cc34f6606d81fa6dc62f94fd244c7a9b37b1b430eb3cbd7c944d90a65d6c451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278053278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9b763015d114f187e3cc76ec452496c6393b37c60712f584044fc7023bf0af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 02:05:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:05:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:05:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:05:05 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:05:05 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:05:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:05:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:05:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:05:19 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:05:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cabbf6008cdae489a5244119baceb06edfd45771866a218db066b2e8457e134`  
		Last Modified: Sat, 17 Jan 2026 13:30:35 GMT  
		Size: 156.1 MB (156107636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37efc2ca7d27fb46e7ecd91ae46db4c4be71c80cf9302f905920ad94409f919a`  
		Last Modified: Fri, 16 Jan 2026 02:05:58 GMT  
		Size: 69.7 MB (69686830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4eea73ec73d5184ab1915e9e38f769d3d3afd00ffa995f5ce3aef13d27ebfa4`  
		Last Modified: Fri, 16 Jan 2026 02:05:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43139183168656dbb2cd8ab0394833a04f7eaca870e0a188e3f48ef14a092d1`  
		Last Modified: Fri, 16 Jan 2026 02:05:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:69e5b16655338dc3ec419588ba52ce753bcbfdbda42588082dff14460ec6ac32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452133216ef4344d9d61e848070718f86f95ee5a3597fad7e2a5ac06ca3b4af6`

```dockerfile
```

-	Layers:
	-	`sha256:e96829de23cb252debf18dc0cdb95f6928802c5fb506da02cc99055b529d4f7e`  
		Last Modified: Fri, 16 Jan 2026 04:45:29 GMT  
		Size: 7.4 MB (7403870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9563ef682b4c8e1a1d595b21d3ce272b931385faf7a2d61f757c261d01a4267a`  
		Last Modified: Fri, 16 Jan 2026 04:45:30 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
