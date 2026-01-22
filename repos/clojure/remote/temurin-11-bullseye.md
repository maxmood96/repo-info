## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:eeacec9c2aa650956ddcb3e41fdf2de7455ad56849514aa91456d97730aec599
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b6f9048fdb045df100f2398760d644d52277f7fcb88db60abbed6e1a3518ad9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 MB (268280590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89b24f2931a5b44eb9111be9bfaaf346d9b794956803db57806d8c9ff79a2c8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:49:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:49:23 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:49:23 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:49:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:49:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:49:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fb8cd2fbdc0bd4c35e1faae2217e2b7b6ced3d0dc360df6676162fc777d623`  
		Last Modified: Fri, 16 Jan 2026 01:50:00 GMT  
		Size: 145.0 MB (144966589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963ca7c9b8c98fdd5baca7ebdfc33abf03c82ebace2b1132885cb146afc25c4f`  
		Last Modified: Fri, 16 Jan 2026 01:49:59 GMT  
		Size: 69.6 MB (69556911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8610aa9e764e1ae9393591cc755a20b9466d3dfba70cbf45fd0133e6d475bbe`  
		Last Modified: Fri, 16 Jan 2026 01:49:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9ca2d7d1314fe940ee738682fb5ee84eb8c5b7e24c0b2bcb52d33f60d4bce6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35dab4855af27da09d1e1d20ffdd7d1a682c63382f3007df2e7da890af5951f`

```dockerfile
```

-	Layers:
	-	`sha256:d11078607ada8705a185f34edb1f789cf94236e7eef3a4e707780bbb022df386`  
		Last Modified: Fri, 16 Jan 2026 04:36:51 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69e5e643be7b9b1eb0947185c12deef42c8450a5234a05d80318385d3a9be3d3`  
		Last Modified: Fri, 16 Jan 2026 01:49:56 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ccbae89d166680081ebf62e32c7762e78a5a1f6c4d67b910c7dd4be6fc8b9f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263675071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1879d984e2f12e16055fcb6547d0db98fb532e457a513dc98259a8d06cd673e6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:53:20 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:53:20 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:53:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:53:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:53:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a8ae18596296256359f5311b1ea2be7af7a51f52139f7ec0cd756e2f466805`  
		Last Modified: Fri, 16 Jan 2026 01:53:58 GMT  
		Size: 141.7 MB (141729881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bdc97d46130d54387c527fcb7eb54e46566c91d760177996d8f228b3ad2c72`  
		Last Modified: Fri, 16 Jan 2026 01:54:11 GMT  
		Size: 69.7 MB (69686775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651d760438f04ae654cc09141d3e0c44d13d2e96839a8e9b86742e69186e742b`  
		Last Modified: Fri, 16 Jan 2026 01:54:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1ee9e9d755927927f339e9788ed6d6b35b3d7529acb0fddbdec745c0f5440ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34892a71b017f582341a6bbc083f27ee49680084b05e198dfb607093e1e174e`

```dockerfile
```

-	Layers:
	-	`sha256:a4dcc7d1440f6716e5074f989b0784e8551c05e9cfece9c5f392fb215841a039`  
		Last Modified: Fri, 16 Jan 2026 04:36:58 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c29048dedab20402c84397ba6435354d616bc7f8ef524ef5e91496a39629f7c`  
		Last Modified: Fri, 16 Jan 2026 04:36:59 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
