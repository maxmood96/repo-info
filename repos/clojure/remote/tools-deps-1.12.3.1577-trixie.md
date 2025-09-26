## `clojure:tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:9eb4422d44e417e1a9885fdeea59263628c73269527d038d64c8baf9de192a12
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

### `clojure:tools-deps-1.12.3.1577-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:a63f40112d342e711d14d513129f3b4d0a59e3fb501eac20974a974d7d07e032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226857486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb7e319f00970a5021a5dcc36767a54bdf66b16f462a1683181b968e6f14d95`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c67ff1f1ef606724e6ef1009999d95eb7c44ec04ea0eff95eb9db0d69042a4`  
		Last Modified: Fri, 26 Sep 2025 17:59:41 GMT  
		Size: 92.0 MB (92036050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c72a45afb5c14d81db4446c7443b8997200108ac849c3899cd91da4272dbf6`  
		Last Modified: Fri, 26 Sep 2025 17:59:41 GMT  
		Size: 85.5 MB (85540865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6eb60715ef32b1d7f2cb2f5b16b206271f58878da68edc7069ce51650c4904f`  
		Last Modified: Fri, 26 Sep 2025 17:59:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c08e0059141ddc549bd262416fc5440efc0f2bbb8ac21776a99c5846faac3e`  
		Last Modified: Fri, 26 Sep 2025 17:59:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ca6dd3bd45c08c606f99874df40f4d8834c7334b3bc946aa56e021737577d5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1470f6a3feae79ec152ef2e0b69a99fa71ba4cfd2cb5a3f1b49d172e257cea3`

```dockerfile
```

-	Layers:
	-	`sha256:310fb9ce0003eb04eed908a394a5666392607b7e3d69138b405df42315c093b0`  
		Last Modified: Fri, 26 Sep 2025 18:45:40 GMT  
		Size: 7.4 MB (7418163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dbb83eb5c6273e489c572f0140fc9c0c105e0c7ed287b1de90b544376917b23`  
		Last Modified: Fri, 26 Sep 2025 18:45:41 GMT  
		Size: 16.5 KB (16458 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0dcd6cddd0900475ef41352d371704192fd7a1d9fdac8338ba70b80568a9eed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226053493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa6cb2258854a4cd2ee7ca1c32fc6ff80639c7bab49c4c77e5bb8020e0be1f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28484d7db774aef0b86a84c8c98372727ce34d337cf58d2c72528e5487e3fb0d`  
		Last Modified: Fri, 26 Sep 2025 17:53:20 GMT  
		Size: 91.0 MB (91045228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3dd93fe34f6e216d7e63764395ac6d203ad6b0e5b35e75d7c006f6b165f520`  
		Last Modified: Fri, 26 Sep 2025 17:53:20 GMT  
		Size: 85.4 MB (85363480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806c3e473b966373ff58df884ccbc2618781afaad1ad681c87e1e2f92c2364c5`  
		Last Modified: Fri, 26 Sep 2025 18:42:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b4e0d5217c7fa167995d9b529b1e5d73dc6d356ac36f878d6a901774cd2353`  
		Last Modified: Fri, 26 Sep 2025 18:42:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cf41fecf538c15330b94421b92a1697502b68730bf727c53baf1add492e81727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e3ef2b3b730a1f093e482dde45f71df2180354e3d113af442a3c5f5dadfbbb`

```dockerfile
```

-	Layers:
	-	`sha256:c063312c93b2ccfc30a4a91628b6431b9914ee25876d6fbd1ddf3d7b236abd0d`  
		Last Modified: Fri, 26 Sep 2025 18:45:52 GMT  
		Size: 7.4 MB (7425214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57dd585da3913be265d438ab41841521e6e61d212b06dd98b6d924bbc9380ef3`  
		Last Modified: Fri, 26 Sep 2025 18:45:52 GMT  
		Size: 16.6 KB (16599 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b539d9d24dc8b13392423f22469c195961ab2410b5feea8c01320bcb90a5c2a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235655576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6290174eb8d12ed46edb47ebee543e30743c1aeb49ea012446d74ad14bf95cc1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cf4ae381b4e7bb5c15181abe64e994932533643478b9004c85a25713722adb`  
		Last Modified: Fri, 26 Sep 2025 18:35:32 GMT  
		Size: 91.6 MB (91601719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8d150849f5b629824b18994694bebd851266b221e785163add4b32fe206466`  
		Last Modified: Fri, 26 Sep 2025 18:42:39 GMT  
		Size: 90.9 MB (90948382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adb89407fcc5784cc09e9368a3d8d14df13f62d30ebc1e1b2eb2699ec38114c`  
		Last Modified: Fri, 26 Sep 2025 18:42:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a837727eff26b61b83c4dc26751c3ce5b6bb33d35e21702b16916e5b077f9d9`  
		Last Modified: Fri, 26 Sep 2025 18:42:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:08bb38313ca6db3c23e09e4686a8e00b1fdbe21e3d4eb7b79b34904f1dd84979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1c5b8ebda4d34ade1c2dd3d424332b4c790f46b767e03b999bed95bfabf95b`

```dockerfile
```

-	Layers:
	-	`sha256:bab6f3113e05e3cd07a0edc27575fba70885a4f275ee828bd84a21a8349dcc13`  
		Last Modified: Fri, 26 Sep 2025 21:42:18 GMT  
		Size: 7.4 MB (7423892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b31150fc579ffee7fbac13c48497c0ae43cc0b0c36cdfcc076f7ec5788ec8`  
		Last Modified: Fri, 26 Sep 2025 21:42:19 GMT  
		Size: 16.5 KB (16518 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:b8dcba84da60bb0804b3a08d6098f8e1ec02f03ebbfe3e0905af9efa9af93251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224061044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6944b2668fec53290279dbcf1f99826f07e0c21020dac154d0595cf850b91516`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182ac8820269436dcc9484ffc51122fcc381e8185984b2a97426f0cdc265d933`  
		Last Modified: Fri, 26 Sep 2025 19:34:05 GMT  
		Size: 88.2 MB (88206458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ac7c31a9ca64f50e065b17c599ded0ea5487cc4a7f934c82ec901c67a126e8`  
		Last Modified: Fri, 26 Sep 2025 19:43:18 GMT  
		Size: 86.5 MB (86507214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07b7b8475464028500117dad358d5065d45ba9c8685b97e8029f8722d5b0d93`  
		Last Modified: Fri, 26 Sep 2025 19:43:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0560ab376e619834ba0af76f100af3563c091bda3ed01e8ce947f3bff3508706`  
		Last Modified: Fri, 26 Sep 2025 19:43:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e1b44558d104af8dcda2d56e0bb7caa14599816c537caabd52b59da491c8c3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd5dace5af8a5bd98cfd27a5ce0a6643875d9930cbc1bb28c1f305617a3a2b4`

```dockerfile
```

-	Layers:
	-	`sha256:8d8acda67303685882ad3145e2ed66b555ad233cff86b5091616de3688791d3f`  
		Last Modified: Fri, 26 Sep 2025 21:42:24 GMT  
		Size: 7.4 MB (7416633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a39eae24059e5d5c7d4e4479478f4a6ce2ec8f8a39de72048bcc669645f5c50`  
		Last Modified: Fri, 26 Sep 2025 21:42:24 GMT  
		Size: 16.5 KB (16457 bytes)  
		MIME: application/vnd.in-toto+json
