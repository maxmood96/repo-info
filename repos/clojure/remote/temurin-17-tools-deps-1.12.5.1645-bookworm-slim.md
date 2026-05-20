## `clojure:temurin-17-tools-deps-1.12.5.1645-bookworm-slim`

```console
$ docker pull clojure@sha256:d286f7888591b2fc740ccd81cff26b4ecb264b561297d79bc6a4801f93d704fb
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

### `clojure:temurin-17-tools-deps-1.12.5.1645-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c3049ddc121f0780b40413469fe4b5881d225450e290bf1130a20e323b9bb56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243877527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6c2512cb88178e2583feb2fc97bb7021fdbe84624dcb91fca3363a7ee8d8f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:58:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:58:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:58:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:58:57 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:58:57 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:59:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:59:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:59:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:59:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:59:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a585ed0844e65030e6439305979d463e640b0da9c7a47b5e6effc3b8d012695`  
		Last Modified: Tue, 19 May 2026 23:59:31 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cde2c08a2481446edc31bc99247155b0b33e8409d42ad99e7d3991170342c80`  
		Last Modified: Tue, 19 May 2026 23:59:33 GMT  
		Size: 69.7 MB (69737487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4be4aab75e7b6d2a5ce42ad0cb82523435809c11393d41ccc961acf34f369b4`  
		Last Modified: Tue, 19 May 2026 23:59:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f30f1413c5a19e117a93e80931e3a648cdd6a977e20c22da9a683c3d87142d0`  
		Last Modified: Tue, 19 May 2026 23:59:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ac488ee5df2494993f65f6ce803e56af06d2de2a5185508207134122c67bb122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b22a2a738a4eb1095136e1107f0f5ed96ac83a7295a2bc811ecb44e8de1060`

```dockerfile
```

-	Layers:
	-	`sha256:3ee3b6eaf0ef12c7e028ccaadd6586d3f662a857591467eace10f4dece94d4c1`  
		Last Modified: Tue, 19 May 2026 23:59:30 GMT  
		Size: 5.1 MB (5116814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14cd20ebb2acd5bd155f63411ea4508e62d3e6adeb4ae6c6ac7e289a8a901092`  
		Last Modified: Tue, 19 May 2026 23:59:30 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1645-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8f7425a7ca39f4a454c4113bf8ea30454d4a59728145248d68f073bcf90f94d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242571939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a261f46087e4ee027a805e81cbc3b5789de4002018038de4200e2dc9e3c696a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:06:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:06:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:06:03 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:06:03 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:06:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:06:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:06:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:06:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:06:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a15e87843ef81384ee279525ccd410db54ecb3c473ec2ab820fa9f71fe5b20`  
		Last Modified: Wed, 20 May 2026 00:06:40 GMT  
		Size: 144.7 MB (144724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215002808f64e1cfb96f5400e2e3727140b84c78f6b8c8995c669fea058be6ac`  
		Last Modified: Wed, 20 May 2026 00:06:39 GMT  
		Size: 69.7 MB (69731496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f01ce36f16531a15808665f3168ee6d36a1e4a2b96ccb1500316763dd0d2fd`  
		Last Modified: Wed, 20 May 2026 00:06:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc217fede201dcbfd1036f957cb4c1763392294bc367e29e72e610cc34f645c`  
		Last Modified: Wed, 20 May 2026 00:06:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:32fe71fd6b7ac790e438268687a48288f19c144c511b44e2734ad3b54603e388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cfedd971baf57093a930ca287f18b97ae294521461b9dd63135ef248601ace`

```dockerfile
```

-	Layers:
	-	`sha256:18c4e35aa773e6df7fc855749638a5d13971c1b206cf36e0b864b8c33777370e`  
		Last Modified: Wed, 20 May 2026 00:06:36 GMT  
		Size: 5.1 MB (5122575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c55fae4a59c4723f438761850b69c6dfeafc48d986b51c25ee971e757d30573b`  
		Last Modified: Wed, 20 May 2026 00:06:35 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1645-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:43d5daab0ba0c213d4e9ce1b9f45713c616be4128757ecf276c4098ad7897c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253414778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b4af3ecdf54607251969089f5b6b844cb720a60aca183f0322f9ff79b5f52bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:54:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:54:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:54:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:54:25 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 05:54:25 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:58:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 05:58:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 05:58:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 05:58:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 05:58:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6633021a99f451d585b657cbca0d3fbc241ffb487dcadb3e2ad6afd10c777642`  
		Last Modified: Wed, 20 May 2026 05:55:35 GMT  
		Size: 145.8 MB (145766094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d8699796f931afe5367c6f101b01760926a96aff9c6f43e8aabfcff4b5f357`  
		Last Modified: Wed, 20 May 2026 05:58:46 GMT  
		Size: 75.6 MB (75571903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f42653ec89ed9681a4e2ee246345897849886be324fb613a48f12a15d18eab9`  
		Last Modified: Wed, 20 May 2026 05:58:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5339d856d6492d5d5687e5a44e06fabb2704c6214279e0a2651d479bf212dda`  
		Last Modified: Wed, 20 May 2026 05:58:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f4841dacda0796b21d4a6e30910c1e43d9269d4e2773fdf42770c1919f7411b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1b1f14ad86f688ade0c06583626d57e550b5173f36b5259d0dd9a68452cfa3`

```dockerfile
```

-	Layers:
	-	`sha256:8b5168dc386e07ab5cceec175f62ab8c9fc8485682da4a569482cc6181004cc1`  
		Last Modified: Wed, 20 May 2026 05:58:44 GMT  
		Size: 5.1 MB (5121972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7941bff5aadfa0adf42f2a2bc98d4f2c411949f15e2274960a74056da6404d14`  
		Last Modified: Wed, 20 May 2026 05:58:43 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1645-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b21eec8e399e46c15f2cdfbbfe0fb8b9407dcb02405ea8814e5b807700df4f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231339257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f6425e2eaa3bd7c5490f01abb43d06743001f02e59c9a0d60e51defe718c5d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:43:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:43:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:43:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:43:34 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:43:34 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:44:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:44:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:44:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:44:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:44:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98599326617712457c00a2d8bdb39c7b97547607326c3b68b05c08a2af0c0e96`  
		Last Modified: Wed, 20 May 2026 01:44:14 GMT  
		Size: 135.9 MB (135910447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac0313ee811172625b683503d0e9443364a418dfe5f3f59e2a65538eb3425dd`  
		Last Modified: Wed, 20 May 2026 01:45:08 GMT  
		Size: 68.5 MB (68539171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcc99ad423e190888e1db021ae2ad26e25917918af2420a0239580889280d22`  
		Last Modified: Wed, 20 May 2026 01:45:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb87d52d3c003b50a9e956c84a7a3c0581c1610dae17e8ec379bb4bbb59acd7`  
		Last Modified: Wed, 20 May 2026 01:45:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2bd95c4a6faf0a88d2fa5918d3e99a9f5ce376409df5ee1ff5a9756bdb3b82ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5124124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47cd56f3715b0d36871836ee41541e9f6786adb8833f0c91108afdac1056c803`

```dockerfile
```

-	Layers:
	-	`sha256:23cd4118681a591c821b15b7e2ae82d46a47d830d7b957378102ef1d585ee3e4`  
		Last Modified: Wed, 20 May 2026 01:45:07 GMT  
		Size: 5.1 MB (5108135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dcc2f6009d614e68ef84a92291a10744f363fd12ac5f1bce0fffb8c33be2a56`  
		Last Modified: Wed, 20 May 2026 01:45:07 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json
