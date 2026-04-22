## `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:f3a6b7d09aba73dde68709e141e094be2ca80de7391985910569d82cafb3f8d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b7bbaa7d97e126972ce4450e70634fe8b8f3bba1d54ef05a99f9ca82c6ce7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247599036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e9a35636edcd2131565386e920f634f8af9aa139480496b304fa80e522792c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:17:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:17:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:17:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:17:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:17:45 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:18:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:18:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:18:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbead252121f678f19044f65f95a368c7ec289869721f77580f80c26acbf16c`  
		Last Modified: Wed, 22 Apr 2026 02:18:26 GMT  
		Size: 145.8 MB (145806833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a12f81c9122a128636d45ded4ae78d2fcd4f3aa3580fac0601f6ed7abd4a6a4`  
		Last Modified: Wed, 22 Apr 2026 02:18:24 GMT  
		Size: 72.0 MB (72011385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5e33f67a32ef89102bdb0ac0a69e5a911be1f50d17ab9657e48848def8644c`  
		Last Modified: Wed, 22 Apr 2026 02:18:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a8f208f1f329be2093df424e16aa578c5d96df4b117bad69dbdc32b1844a0261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886df7e287fafe77f7c95b05ed79b36957401304c6eb153fba0ac5ecd98aae70`

```dockerfile
```

-	Layers:
	-	`sha256:30b47dfe3a3269141aa0ff0b3890c8b9a3d77db3515b08725a56e4dfc63aa4a6`  
		Last Modified: Wed, 22 Apr 2026 02:18:21 GMT  
		Size: 5.3 MB (5279333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f0d9e94d101c7ac9966c508092358b209bd600973e9ab3f86a3cb59012d3c1`  
		Last Modified: Wed, 22 Apr 2026 02:18:20 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:39fa476023cf7167b9824f2a66c8a55201eec9e17a188ad038e4fa1995c5b6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244475856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927ec28d57a10136d17d6636202d91480db064c6d559a090cdcdee3bcadacbf6`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:20:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:20:51 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190a74c976dc2438d09255b2962f7eb86d09cc2d8561ac235b8194f95326fa14`  
		Last Modified: Wed, 22 Apr 2026 02:21:31 GMT  
		Size: 142.5 MB (142500802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23551bc95003a80fbd24948fae8a57fe08d1f46234610449ed77798451ccce17`  
		Last Modified: Wed, 22 Apr 2026 02:21:29 GMT  
		Size: 71.8 MB (71830804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d23dd77094b844d2e8efb0e95cb108e500ea1b4aa13bab6c7accb0bcb9cee5`  
		Last Modified: Wed, 22 Apr 2026 02:21:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8067264e0e60779d22ef64678c2a7a9cf4e057e47123081a895521f6a278448a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83fe0dae605e61dcec575bde7316577a6c4057f6f1a3e4a64879941dcae7287`

```dockerfile
```

-	Layers:
	-	`sha256:2cfb6a1639a0fe71b02ac59203d4b0309525b0a24512e291a3ac3733af5c3114`  
		Last Modified: Wed, 22 Apr 2026 02:21:27 GMT  
		Size: 5.3 MB (5285720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b91f7dac3392f4a6c5d50dc518d20704b09b0fe493a1b8328e5efc763c894d`  
		Last Modified: Wed, 22 Apr 2026 02:21:26 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3522fc4d9cef901496ad7504b5a738d81ba876e42a8a43ecf13c623facd2ee67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247201387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d092cfeb83996b1209a4fa5e39d0aa65be3f07660952d1df91b15671494e009`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 02:42:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:42:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:42:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:42:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:42:14 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:48:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:48:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:48:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76042bd72cd27c05c77d44bd98d120db7be804788d7f01116ecc64346fb992b6`  
		Last Modified: Thu, 16 Apr 2026 02:43:49 GMT  
		Size: 133.0 MB (132997414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f654998ceab4a801a39fade9f3743f1efe6e5172d489c2c6cbd8c6fed240b3`  
		Last Modified: Thu, 16 Apr 2026 02:48:47 GMT  
		Size: 80.6 MB (80610309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6086fa06102084aa8ec5e00e7262867ff3567ad9c96ee6ddc33d0f7226dcd7a`  
		Last Modified: Thu, 16 Apr 2026 02:48:45 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d9eb1c37a17b60da98c1f4f33830f84fd03ac98e3f823589e645a8afaf62c37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4830f54a59a5f58c87c71420f2674d67ecfc377099c3f7b5d337fc446b163f41`

```dockerfile
```

-	Layers:
	-	`sha256:dd6ca91153023e2a8128e59f52dec1d9dd53a7e8844236678229039c04948bd2`  
		Last Modified: Thu, 16 Apr 2026 02:48:46 GMT  
		Size: 5.3 MB (5283035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f296a7684a405afb228344d31f81a1462f76a9e7f3ed1d4fe4d1f2b8928aa4f`  
		Last Modified: Thu, 16 Apr 2026 02:48:45 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f96d5d5744ffb13894a9d2e085af71b10c4e6fbff823d11cf219887dcc00e9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229390080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aea2de0fecea4c95e621d5e498317fd380090a20e2eac12f65b316135a68d2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:58:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 03:58:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 03:58:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:58:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 03:58:52 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:00:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:00:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:00:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1864f84ed444e2e225dd014a08920525f5def284ae07e65ec1d3d4c0da23d26`  
		Last Modified: Wed, 22 Apr 2026 03:59:29 GMT  
		Size: 126.6 MB (126562155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a2f74ac7ac2df883f11f8fdceb1aaed36d97e6a0e6e805820a2c14dd8c2e59`  
		Last Modified: Wed, 22 Apr 2026 04:00:27 GMT  
		Size: 73.0 MB (72986979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff745dabdf01914a0330e65bb9855c43956aaedccf85ec041ab8d312bb18c185`  
		Last Modified: Wed, 22 Apr 2026 04:00:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:88a5165a344a4ef36481809ee11902103699353a6f15ee7c06d237d45feca90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c07a089685c02296fca123a26bc1b9b75067cfe27cae3a9c6f1f6c8102c6448`

```dockerfile
```

-	Layers:
	-	`sha256:684d178193260769e34948376b591255e1b9be95d2e609234435661c45a730a4`  
		Last Modified: Wed, 22 Apr 2026 04:00:31 GMT  
		Size: 5.3 MB (5275261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4ca927cc97b1fe07f4f33e8fd453ee09e30fd6c595d15e4d65561f24908490`  
		Last Modified: Wed, 22 Apr 2026 04:00:31 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
