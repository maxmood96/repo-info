## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:179101dc0204c569823d01227cd9ee5be5da0efddd1228a15c4b66930563cd55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:265ab82a2045cbd9f676f8338f1ef6f1cd9c6c45118d7a0142354b388b04ee60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184359315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc854a823f22d9960bd1a598b17e2f3925d705b290874e71020648855dcfaa69`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:53:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:53:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:53:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:53:30 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:53:30 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:53:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:53:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:53:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbd38025350fc991110cfe4f6be8b83d231520588c9f88215239d4025b38ee0`  
		Last Modified: Tue, 04 Nov 2025 00:54:16 GMT  
		Size: 54.7 MB (54731292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660494c52fcc2f97b4984c86fdeb213b2527b75e10b3ba9568891542b7195ca3`  
		Last Modified: Tue, 04 Nov 2025 00:54:20 GMT  
		Size: 81.1 MB (81146324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826728b5baf9139ff6d4ea9a3274054c074257fc4fac18cd85fc33a1162f1635`  
		Last Modified: Tue, 04 Nov 2025 00:54:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:638966d59fc3f811790f49506e8bbdac3cb65754275cc59e5e02ef53d21338d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24c5694b02a22124aeaa93ce127a601f5e7964ec77647100aec99e8ad2ccdec`

```dockerfile
```

-	Layers:
	-	`sha256:bede176b4a6e2155f1d55b460f2c87a20f5c2afb255ed41d203322b11fe8ee89`  
		Last Modified: Tue, 04 Nov 2025 10:47:34 GMT  
		Size: 7.5 MB (7496500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f13bbd73472c3372df80fd03650453a51f50988e4d825d190d6a066c273ff7be`  
		Last Modified: Tue, 04 Nov 2025 10:47:35 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a5c8a44e3b1e7e2cd4026d255aee069e5e630f620d62d23ab0e0578ddddb9082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183226693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0464e8c931e3bfda2017954d5edc66b92096e8b2305f8235bc67a82aff30d207`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:53:20 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:54:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:54:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:54:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a154cb0ba147b5df1aeb2b250e00f93a83dada5d99427da6face1d784dcdf3f4`  
		Last Modified: Tue, 04 Nov 2025 00:54:11 GMT  
		Size: 53.8 MB (53835577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842867a29bd522f874d2d22c262cd4c05a92f789958daaf21242ec468c258deb`  
		Last Modified: Tue, 04 Nov 2025 00:54:47 GMT  
		Size: 81.0 MB (81030995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7257baec781130d7ee5772dc78e0b338a350414e793367ccfecd564f74c4ea06`  
		Last Modified: Tue, 04 Nov 2025 00:54:40 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:85597df18723db5cc011afa17833d47cc553f8e2ec42a859724cfec7ed759800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b213d1e1193bb295e703c9ac96801e1f04a3a225dded71b295be1272982602`

```dockerfile
```

-	Layers:
	-	`sha256:b4139893cac4863047a7e6958681998f77d6d56c9fee08f3cacec01b4ab29d1a`  
		Last Modified: Tue, 04 Nov 2025 10:47:42 GMT  
		Size: 7.5 MB (7502961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1ce5cc26e135044fac546385d2fdc7366928d4a20bd1d382972ec55d1f42b4`  
		Last Modified: Tue, 04 Nov 2025 10:47:43 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:126425f1475efcc665547a4444a6b40ca5db2058af6a7a71555414d878388925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191479471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7f31a5ebc2002d623f5a1613225349fc96023245d1d0e615cdaaa21c9e0436`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:41:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:41:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:41:11 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:41:11 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:43:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:43:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:43:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e087d3813ccc9e7760d17d16b718f6640f07dd3d84b7f82505a7931918e504`  
		Last Modified: Tue, 04 Nov 2025 00:42:40 GMT  
		Size: 52.2 MB (52165399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98d88f440a3027e95e8325e14344aa5d4f86d6ca8575ea245ae091fbdfb3813`  
		Last Modified: Tue, 04 Nov 2025 00:44:41 GMT  
		Size: 87.0 MB (86986145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40dc8e82ccc8eaa72c778b3c30bd1e7d3d0b13501c82a25d84beb87246c5148`  
		Last Modified: Tue, 04 Nov 2025 00:44:32 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:34f44ff45bc6c38e451f1b2ad68976cceda108d41131bc09319527081df93585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7515749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eab861dee3c4e2ae0e7c9541a963c953ae271320d7479d5bdc9b1fbd3d39bcc`

```dockerfile
```

-	Layers:
	-	`sha256:7c1630fad4c4d115861317411d836bc4bc6c4887eb34c028383a60bfa6bdccb7`  
		Last Modified: Tue, 04 Nov 2025 10:47:59 GMT  
		Size: 7.5 MB (7502307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd1463c53f88aac4eb8b29fdab33c86163f4b37899f5f452726d852e12a40e6`  
		Last Modified: Tue, 04 Nov 2025 10:47:59 GMT  
		Size: 13.4 KB (13442 bytes)  
		MIME: application/vnd.in-toto+json
