## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:476114705ef0c6dae94960b48a988e78b21f15a67f5fe85da9292eae76c24ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:25e2009c41df98a8d09178df6cbc71413ccd1bcca533631841d732db719d2516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280784555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a297d5aa7138427988a4ba9b7b97651889541f9e18dceefdce067044851eae8b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbcf0121effd54c7f197f530e95e9367501fd9a9ff47ac82c28db4e50421392`  
		Last Modified: Tue, 03 Jun 2025 17:57:57 GMT  
		Size: 157.6 MB (157634492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8fdde9c15cdb20911c20df33dec0469b437f4b1f732d9c24734c198e7c4b6f`  
		Last Modified: Tue, 03 Jun 2025 17:57:50 GMT  
		Size: 69.4 MB (69398830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3d67cf92cc1926407781a36ce43f7223afd3708eac6c34ed3b740b73b99a98`  
		Last Modified: Tue, 03 Jun 2025 17:57:43 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461a0e5339e08b2d2ce9f102dab8ff312b4a190cbb7b62ccb7e264f8f116d719`  
		Last Modified: Tue, 03 Jun 2025 17:57:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2524ffad629077abe65204c463773150c881f376769a308d2a5f0b5dfa932ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7276461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808729494b111e1b027e670d86ab58fcb7cb100d299f10e0092cf7c031d41235`

```dockerfile
```

-	Layers:
	-	`sha256:1f3e4c55bfe6646805b2779cc087cd93e3b619589761267d8dc01e7220013e6b`  
		Last Modified: Tue, 03 Jun 2025 05:16:39 GMT  
		Size: 7.3 MB (7259964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7a9dbae2fdb820afd06f2f9debd9a2746d344f7ca28daaa12e857bb7189a9a3`  
		Last Modified: Tue, 03 Jun 2025 05:16:38 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a704ff3ce69762dd69d5974947708c470e8461bdceec4770b9a3cf74bc97a9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277708224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f61f54ef2d9c7b564e74659229f3aef74ce4132da62dbbcad55cc87285f037a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a5e26e3cb5abfbd307a69d846765430705dd9214f5910e9a937311871d3dc9`  
		Last Modified: Tue, 03 Jun 2025 10:53:55 GMT  
		Size: 155.9 MB (155928831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458c5d024f07fee3ace22f2593adc9398bc3a987bcd29246281e7bea655a95e7`  
		Last Modified: Tue, 03 Jun 2025 11:00:15 GMT  
		Size: 69.5 MB (69530598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57840e42219844e60d6f6d3c0c076e16dba05aba4cec719ad175d7608d6d3d35`  
		Last Modified: Tue, 03 Jun 2025 11:00:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a07eb59a21ffe13daf8c4f1a2041e1a27950fafa695bd1ed9af429f2367de7b`  
		Last Modified: Tue, 03 Jun 2025 11:00:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9811c129d1b082bd5da696898a73f721ce5c3d7ec84da7e705c661405771243c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7281726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31d0bf54e659e20f23bddf4e353f15f9d361223e437e29179c2ff12d306a55b`

```dockerfile
```

-	Layers:
	-	`sha256:394dacea3727c4060e9b7df86cdf5d91940b35233add83cd91cd4f011683b15e`  
		Last Modified: Tue, 03 Jun 2025 18:38:58 GMT  
		Size: 7.3 MB (7265087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75ee34b260ace9ba3e8d51f280dfe75561b9d23143e7e8bdf434607d55c2b2e`  
		Last Modified: Tue, 03 Jun 2025 18:38:59 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
