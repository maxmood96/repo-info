## `clojure:tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:abc8eef02750a5befc6bfd969d5083ff30b096ce033bc22f57814598b3147ed3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps-1.12.3.1577-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:fdfb6d31a95c9c2470b8070b3f984367d580b0ca350615e66bb065570e267f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229820346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec876e0a599da8c722c5429c119fb4e07dea986b24ed036ea638f3a3db81d33`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444b898a839c6308dfa59bbbf580bca17ad8f3de6c4eff7c095ff76c8b880ccc`  
		Last Modified: Fri, 10 Oct 2025 03:56:21 GMT  
		Size: 92.0 MB (92036030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be2881be139d189c88e9890ee557ffa02ff751d3d7f96421fd537b61f1df647`  
		Last Modified: Fri, 10 Oct 2025 03:56:20 GMT  
		Size: 88.5 MB (88498647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88508c0476e8f787c7f90527ab14e97da101ee5b449de48d8c3d4094b68e9b10`  
		Last Modified: Thu, 09 Oct 2025 23:14:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b29cbd30f6685bbf90f6d06cc22f3ab0c05a43c05922e7874a11290e256ced`  
		Last Modified: Thu, 09 Oct 2025 23:14:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4c0570a95b4825275ca96bcdb4f520f770f2a94b9da17bafe0c4144ace0e6889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487689768cbbbe49991319152ff0b2128e87ccb6fb6f8462217815c9f46021af`

```dockerfile
```

-	Layers:
	-	`sha256:2470005c6ec2c77c4fc66d80b15cb6268b794b59f8a265c8aa99c02ec51f6cd6`  
		Last Modified: Fri, 10 Oct 2025 06:49:06 GMT  
		Size: 7.4 MB (7418217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c50e4488fc1388438221fcdace730c5e937b5b8b85f99dcf2103aab5bb451ddb`  
		Last Modified: Fri, 10 Oct 2025 06:49:07 GMT  
		Size: 16.5 KB (16458 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2d6247f493e1820b496d1d93da694ba039e830b34828e4a3fd6d9f61f72a22d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229385630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541c900a3a0d7a51fea2f0f05a8a4ab9c6ec0d476453b7ae88fbc95506016411`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38739bd20d171b318f46126a8de2bbff90bacff2b69419a0a4c4cbd8048ccff`  
		Last Modified: Thu, 09 Oct 2025 22:31:28 GMT  
		Size: 91.0 MB (91045227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5be4ab3560cbf7f8512b5a6a8091480426401f2000aa92e85a99c3f585ce9e`  
		Last Modified: Thu, 09 Oct 2025 22:31:27 GMT  
		Size: 88.7 MB (88690667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae53b99fdc682f3f35cd0b057e4e90290d9445c20cfa8cb8359bcce1b62ae3a`  
		Last Modified: Thu, 09 Oct 2025 22:31:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d14398471374d2606767162770ed247b73329359a5f4a01c81d8ece4ec219c5`  
		Last Modified: Thu, 09 Oct 2025 22:31:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0446a33497d201784505fc60f758910a6c4646186d51258b97a71be9dec34581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07207b7134791a650de3134befbb83653735b825a1d60c6f2999079ee4f228b6`

```dockerfile
```

-	Layers:
	-	`sha256:c659172ec56d96eb76e7d93f19bbe6674d9f59a76770d037a633f652d3f3ba34`  
		Last Modified: Fri, 10 Oct 2025 06:49:14 GMT  
		Size: 7.4 MB (7425268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d0b438d081def052843012e92db69fbd8ef972dd7973b32b7f3fabb272abdb`  
		Last Modified: Fri, 10 Oct 2025 06:49:14 GMT  
		Size: 16.6 KB (16600 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:5efd5041829966189195fbd96d447d852fd191e46fb9c1220f80d9e7a0929e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238863400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9617a83bcd8623ca7f5b108425b65c7f03ca031ec62f05ed76156eb3a4f49b8c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc92fde2234dc8f32a119fed41daaf6c83b22fa10ffcee1fa59c6b6dee4280b`  
		Last Modified: Fri, 10 Oct 2025 05:55:27 GMT  
		Size: 91.6 MB (91601717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b43cc112095259207d0322906d05bfcc97f724ef14f1fbad24b57739c2e44d`  
		Last Modified: Fri, 10 Oct 2025 06:05:08 GMT  
		Size: 94.2 MB (94151423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e543c8514e99e2f6002ad39b0c3d0162a03d604fcb416b8dc0fc7fa4490799e`  
		Last Modified: Fri, 10 Oct 2025 06:05:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920e4968a8c1f3a2cf04f5f81e2dcd54633ac72ac8a3876a79334953774a4298`  
		Last Modified: Fri, 10 Oct 2025 06:05:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d4867dc79a1e99b4053ff50937b51027b25764f7e69b29fa27e9c71c23a39024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3eb3188376f38cd2865d16f72d8f8ed516ee5f2e59981d102a12befa6c3ab41`

```dockerfile
```

-	Layers:
	-	`sha256:5b20e324ef4faa74061b5746dc3089f7e8ae7b8d72b0f77a5c866a5ecb0026b4`  
		Last Modified: Fri, 10 Oct 2025 06:49:20 GMT  
		Size: 7.4 MB (7423946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff50ff0d6f8195e14e74a05b14260054782a9cf8922697d7adc1c80a001c9756`  
		Last Modified: Fri, 10 Oct 2025 06:49:21 GMT  
		Size: 16.5 KB (16518 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:d61c9a2aa777df4704247823a450f423871d76990b166a868e041b4c7a218d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225572519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c3298100ea3e805dd4c39f116008271da599071fe2ebde85c613d11d924e67`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964f0570909b5b1168e8db033d13313402e740c877ecfa3fc939ead46e3f0584`  
		Last Modified: Sat, 04 Oct 2025 15:08:07 GMT  
		Size: 90.8 MB (90752390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b35e41345536e4b39903100ca4cdd3f1cd7acf09e4312b7d1bd2edbe00e350b`  
		Last Modified: Sat, 04 Oct 2025 15:27:29 GMT  
		Size: 87.0 MB (87049079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0487211216114a1f6954e6acfda39f50103b1ffebf9daabf3c33a41ba892926`  
		Last Modified: Sat, 04 Oct 2025 15:27:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ac32d7d681471435a1d1881ed44230a73fa14cec104f93066036b2f34345cc`  
		Last Modified: Sat, 04 Oct 2025 15:27:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:92008c106bfe231229294922751bdb06a3db2f5a4bed9f8bb5b5723a25fb33a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28db29bb06eddeae36b9c6bb627ee5822d542cb22dcae4f5476ecedd03f144fb`

```dockerfile
```

-	Layers:
	-	`sha256:7a07b76996d742927c7fc1d3bc96709946f4c96fce5d5143afffa7e17bee2c80`  
		Last Modified: Sat, 04 Oct 2025 18:36:55 GMT  
		Size: 7.4 MB (7406139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a7e152d4f82a2aa4bce5e3e9159611a2d9e8a86e5b295692d4367e24143de2d`  
		Last Modified: Sat, 04 Oct 2025 18:36:56 GMT  
		Size: 16.5 KB (16518 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:289b9a776834cb9868f225c36ac5fed6e848bca03f3917b95d3431568df6093f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226684063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6544e1f002257467650a58f2d87759c3f99f4c86fef152c39b03edb239a83d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
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
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c472da08548dcf037f943b616dabad9bb86cbf698dd3af1da4c39e1dc1031b7`  
		Last Modified: Fri, 10 Oct 2025 03:42:21 GMT  
		Size: 88.2 MB (88206430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83036269757bedca8ae87dd13c2e369618f3fd2ed1867c4958e70ab146d3a731`  
		Last Modified: Thu, 09 Oct 2025 23:51:45 GMT  
		Size: 89.1 MB (89125151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca2c9bb8ee0994b08fec82d5fbc151fcfaee47f86b8ab918be05f68ff13a77c`  
		Last Modified: Thu, 09 Oct 2025 23:51:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97803e1302231335318fcff0bbf952ab0ffb5a47aeb4b57a7b0d160df90f47a8`  
		Last Modified: Thu, 09 Oct 2025 23:51:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3e6bbf66a2756b999f26e03aa58fa780c302eb5e528b4b36c310727092ccdc0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5228de3b5a12804321d7b7b2a9357aa6e0ba2b3243436fd2c3a12cff3c2384`

```dockerfile
```

-	Layers:
	-	`sha256:83d959366a289e23ced4883c34cc95d6d9c817733a188c0b3df7ab93e04371b9`  
		Last Modified: Fri, 10 Oct 2025 00:40:48 GMT  
		Size: 7.4 MB (7416687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2971deeffbbe67e7927f6cc8b7743c1d0699c305a431237d94a28079d7c7e236`  
		Last Modified: Fri, 10 Oct 2025 00:40:50 GMT  
		Size: 16.5 KB (16457 bytes)  
		MIME: application/vnd.in-toto+json
