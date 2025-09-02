## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:628544a39bed68915670d0f75d659c8efbfa9eb3932c5b5dd030f9dba203d954
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:de2444b769a0c8c00fdd55882ecf9cc89666d3fbc986b9bc2a93c3b9a0fdb02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184364795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc669b5ddbe2f34c20bb8f41999d23769ef78fe1b4029125daa0230c179e32f5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21d1c110aa8bd0ff975bbb69f58c0d3b1fdba7bbfabaaca571b5c9c6872bfaf`  
		Last Modified: Tue, 02 Sep 2025 13:46:17 GMT  
		Size: 54.7 MB (54731307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbfbc9611b29202930b8f496d6ea0b82cb413a4ce95c33f2fc3262643377129`  
		Last Modified: Tue, 02 Sep 2025 13:46:22 GMT  
		Size: 81.1 MB (81138333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da5b7cf3e21926edb9b7e6efb9e298e8cf0ebef4d1d43ad94b0f4ddaa8c929e`  
		Last Modified: Tue, 02 Sep 2025 01:00:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:296e5686c774f06e12dc7216e14a2132a4a1ebb55fab49a0bb0b6491927f4fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a047cd0e50645dcd6f41afffcc180cd91476c4e8ff09cd73185a3c2c2878253d`

```dockerfile
```

-	Layers:
	-	`sha256:f93185666a1f90150cfeedb00e5f5270644cfbbd669fc4cd82fecd314ea1e91d`  
		Last Modified: Tue, 02 Sep 2025 03:45:16 GMT  
		Size: 7.5 MB (7489907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952032ce622d1b07aec33fbddffb08a0022bb7c16454e89bde7772fd24061c33`  
		Last Modified: Tue, 02 Sep 2025 03:45:18 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c8ce04cc0427ff9fb63991d94bffcc85301af01c7bc82b7e6d97260c0fc30363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183188087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f873c3c7104bfe4041d68bc67f651d085887dc9e445eff878d4bff9dc3b9e87`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f12554d68ef7bf3c94b1af818066c2ee772de89bef5050e2317a8f94d7e274`  
		Last Modified: Tue, 02 Sep 2025 07:33:23 GMT  
		Size: 53.8 MB (53835609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3556afe3529124295d03a046e86a67e0c7f315b715663e50a66812cdfb0edb31`  
		Last Modified: Tue, 02 Sep 2025 07:39:51 GMT  
		Size: 81.0 MB (81009384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299bddf9dc7ec633f6ced0caa00157d982a8b25d5a5ab0d010d213e6c09843d0`  
		Last Modified: Tue, 02 Sep 2025 07:39:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2c13ed4d2ec1f0e8faef947763dcfdf80ee7ba1012e102b5c620ad2dfd743590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1343d155fa943e165d0061b117c4ba9a52cc63a1a24c20ad220147aacf270a`

```dockerfile
```

-	Layers:
	-	`sha256:8e7642e63851820f60428bd272a512c56746e5a0653d88b8ea3f72378b9057ea`  
		Last Modified: Tue, 02 Sep 2025 09:44:15 GMT  
		Size: 7.5 MB (7496368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5d325dd8c9e5137334907d2ec7d4c6d9b68809be28865b5209f7c5e969bf47`  
		Last Modified: Tue, 02 Sep 2025 09:44:16 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:387d55c32e2361298e170f06216a7fcb44043221708f748e058ed613d91bde76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191476886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5488c49f4e1f365c45789407279d2d3581c54bac244bc1a5d92d546b746f7d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1475976d0e99570891c6d1ccbe046e384b4f002a5228ae471f5b283e1cbb9b`  
		Last Modified: Tue, 02 Sep 2025 08:36:18 GMT  
		Size: 52.2 MB (52165418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bfed4233dbc5ac9e92e4ddc7a1661a20863cf4a244f6e418595d67b11122a5`  
		Last Modified: Tue, 02 Sep 2025 08:00:21 GMT  
		Size: 87.0 MB (86972745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc5d8648224c9737c32aaf6ba3f179877afa78e53dee01f529cc30da2661276`  
		Last Modified: Tue, 02 Sep 2025 08:00:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d6997f99e1477f68569dc3dc0e568b8d7e313bc24ca82bf11474ba5543e4da0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffc466607b69c8c2213721cfb4022a8531b018c4c7e3e9142b5ff9a8cbdaaea`

```dockerfile
```

-	Layers:
	-	`sha256:2f5bbe442396cadf74098a68e9d39213c5de4b134cf272fa93a13d431cc9b927`  
		Last Modified: Tue, 02 Sep 2025 09:44:24 GMT  
		Size: 7.5 MB (7495704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94bf5afea90456e30c6c386a3c7df2d9acc2146d8231887cd9c9d2e3a8418ee`  
		Last Modified: Tue, 02 Sep 2025 09:44:25 GMT  
		Size: 14.3 KB (14284 bytes)  
		MIME: application/vnd.in-toto+json
