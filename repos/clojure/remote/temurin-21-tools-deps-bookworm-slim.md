## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:af32ac0f7cf643a9d7f3502ff5e9d2faa031cddf555a0e5bfede0e1b6ed9ad18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b6eda863b0abccf66aa2194b45eaf15dccd36f4981e4cd474ddd4d1862521824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255308675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df34076cd54018d3db0cfe40728605346f322b1f9418535eacc9d9c361ee8378`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dc825e32635690b863b0b3d2e34b23cc4b7dc6a36a7772e78fc41c140fe38d`  
		Last Modified: Tue, 14 Jan 2025 02:44:44 GMT  
		Size: 157.6 MB (157568721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679bee59c6801f6ab8ebd22329e85d1f82d3e37215b819ac64efc1272d29a044`  
		Last Modified: Tue, 14 Jan 2025 02:44:44 GMT  
		Size: 69.5 MB (69526497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48737264da5009528a4f285c8df57962d7b086e247c3206bd0ebfced2ce7c694`  
		Last Modified: Tue, 14 Jan 2025 02:44:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39bb90639cce5d5bbf897bac297e45d32d49bd1afc563188eeeaa06810a6659`  
		Last Modified: Tue, 14 Jan 2025 02:44:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:86e35cd94324c1b5ecffd2b525ee6ba053c43ab065a876ea5c12319a7e16aae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0503eb869333658fcc9c8a373a9c0721f070f7150655214f368551fb4be209`

```dockerfile
```

-	Layers:
	-	`sha256:a3ea97d1cbbc8f82e6104164a7e76c12154744a4356e3b10160acc95821b580a`  
		Last Modified: Tue, 14 Jan 2025 02:44:42 GMT  
		Size: 4.9 MB (4916367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bad5ca6a92d374a1fe20824a265d58fc2abc430c3b09d2b3c6cf7a159f70189b`  
		Last Modified: Tue, 14 Jan 2025 02:44:42 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:98556dead939c8b9c386ee405863204587cfe8a338a19a4d5167a4bf743a5189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253023004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf63999d6b276d8681bd0d63702f8c4e53e9596cc7a40167682c7fc57b259634`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260e6f636d1eb05d00e219fab56e3c7bcc3684217f5d55e0e62a3009ee3468f9`  
		Last Modified: Wed, 25 Dec 2024 07:31:19 GMT  
		Size: 155.8 MB (155793090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d385b61f4a9237d2aedfa7f640cc0c9f7ea0b4b4722ec67d8f61e20197fa6279`  
		Last Modified: Tue, 07 Jan 2025 03:32:11 GMT  
		Size: 69.2 MB (69170153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd605672dd536674fb7b4b093bdccbe765b4c71b8ae290e135f5bdf151813056`  
		Last Modified: Tue, 07 Jan 2025 03:32:09 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8e711da2c6790d02eafc3fae25263e5636b873468089644f5fc506e5140062`  
		Last Modified: Tue, 07 Jan 2025 03:32:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:31e748fa901e79139f5b0595f25dd38a63052ff503beb6ad912f0afd9eff46de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df529dacd482a6af2f1efd256ee40c906ec74ba5de5e57202a63c27cbe477f3`

```dockerfile
```

-	Layers:
	-	`sha256:d6753b35a56dd2860143ac9d8ad9f732318b8a7ead0384dff7bc8762b354577a`  
		Last Modified: Tue, 07 Jan 2025 03:32:09 GMT  
		Size: 4.9 MB (4922152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ef86f9c71272ca25b47dcb627bfac386dbd0ba2f8c766a09bf17645f35556ad`  
		Last Modified: Tue, 07 Jan 2025 03:32:09 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
