## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:2d0692aa9ebcf064ead9df6828400c163366702e9aae5cad960451ecd6177b9f
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

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:97192ba69b8809c4c997028f267fa8eb5ee94d441cd8adb0d5f19819af6b14ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249066015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6c719a9cec6b4cc51e7b5f8bbd93ab1f2851eaaf19b44649ed080cea84d043`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858d6880375674322c08c9949c2a1ba94751613e1a6baf333d362699e7750a04`  
		Last Modified: Tue, 03 Jun 2025 17:18:27 GMT  
		Size: 144.6 MB (144634987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0633d35d00ff520b0e8a3fef4ed0a6c7b31a0324a70d0d40e310739760186a7d`  
		Last Modified: Tue, 03 Jun 2025 17:18:19 GMT  
		Size: 74.7 MB (74674604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd00d628518a016fe5db321ce28db4b94831660407f9fd13f56c44243afd6a0`  
		Last Modified: Tue, 03 Jun 2025 17:18:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540aeb1ab4ec0b7eb30b694a7f13a519e82276782f918d601ce4c7aacd15d04a`  
		Last Modified: Tue, 03 Jun 2025 17:18:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:201d6f75206beaa8508030c3d474945dfb01c1aa36a05d33caebe9cca05c5d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5127920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb107f67585734e92bc7d4999108ec3d2a7d09b5a7e252b4bdabecb72f9c563`

```dockerfile
```

-	Layers:
	-	`sha256:b4e21337bb0908a166652e6b418fb1e4f32affce3917ec6c71a04d34733a0550`  
		Last Modified: Tue, 03 Jun 2025 15:36:44 GMT  
		Size: 5.1 MB (5112065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a16b7947c3b0a09b4178cd01f2952dc42aad4474e25e18e949e52d5930c387`  
		Last Modified: Tue, 03 Jun 2025 15:36:45 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:54521c81c04084f91ebecb0d8c8392c607180f0c88788df675c840f0a5ab1fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248592291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44281312972743ce838f54b64d5a5ddd1e6a8bc9374a155f698ed4ac7f59ac3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aa191031ed8a3c8712cc547eedf7bf4ab856214d4cc0076e445d91663c3142`  
		Last Modified: Tue, 03 Jun 2025 12:51:45 GMT  
		Size: 143.5 MB (143512648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21d41b9889a5d399295967d6e4e165d18831cbe33f92361debf4c08ea68f669`  
		Last Modified: Tue, 03 Jun 2025 12:57:33 GMT  
		Size: 75.0 MB (74959151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec56a98c3969811b249c23a2a6a45b75e3f0043d9b2cced406fc87e4bdf6fd05`  
		Last Modified: Tue, 03 Jun 2025 12:57:30 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b31e82e24ff9ed5a2266523848210a99a3c9977cc739040725e0060925a6a8c`  
		Last Modified: Tue, 03 Jun 2025 12:57:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e30392666f48fcb961305f2691e883ca310dba4831a63817a1abeb30408a4525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482be0363fcf350f70bd5ad7988bf103fdfeaa8d9c235acc5c2d97a7731682d3`

```dockerfile
```

-	Layers:
	-	`sha256:a09c2691e09121948d45c6a3cc2e9d628e1290f498cf1aa6cb3220bd4e2b88f1`  
		Last Modified: Tue, 03 Jun 2025 15:36:50 GMT  
		Size: 5.1 MB (5117834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23fac9d5244b2ca8190c7f6a89040e0d8083fe769b3dd0367f592fabc95415f4`  
		Last Modified: Tue, 03 Jun 2025 15:36:51 GMT  
		Size: 16.0 KB (15972 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:069c2aa2c39cdfed7c56a54ef0492d54dfef08a6a59a504efcd22e71fbc9419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258276225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70bbe9894a5c8f557eb3775244e9a85a54e6f06ace0d7870c243eab3fdb00a0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
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
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Tue, 03 Jun 2025 14:07:09 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe2f8a21171dd5775e8651cab944241a8c5250daaaecb5a5a99444957bad86b`  
		Last Modified: Tue, 03 Jun 2025 08:53:11 GMT  
		Size: 144.3 MB (144280520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e4edf4aa4ff6a54da76cd638f851f5bccdac2efe43e484b01a4428092fea21`  
		Last Modified: Tue, 03 Jun 2025 09:02:37 GMT  
		Size: 80.4 MB (80414099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc60a0a988fe52bbf59675a21f8bc30a3ea3e7a29a58536e69af812ca91664bf`  
		Last Modified: Tue, 03 Jun 2025 09:02:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52412ebf8458e53a22c23718f320846a84fe93f2307d8d377cec6a5a514a10cb`  
		Last Modified: Tue, 03 Jun 2025 09:02:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:553faa9da0849a3117f532666982eacf38a8389ae0188bacc1f27ab2648d3a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c46491e9bd8f218462ddd39dad81697c80d1449c289fcbd75274352650c43f`

```dockerfile
```

-	Layers:
	-	`sha256:08515b01c82eb5aebef2b8e5c0a3f78ca253f8e63eaf4e99439220ad8305ec40`  
		Last Modified: Tue, 03 Jun 2025 15:37:12 GMT  
		Size: 5.1 MB (5116436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c6de81991248d6fda016dc143000d8d5af382cd182b523b5b6f6819f2156ef2`  
		Last Modified: Tue, 03 Jun 2025 15:37:13 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:c6f8e69ef458281e94fb7e947647119169e519cd7bcbb5828924f0c0fb351047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (240029894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d1053b5912f24b9a5e896db9e12a3fedabdbcb45163bcafe7255e7abbafbf1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
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
	-	`sha256:f092cb6a76bde9a7b3c337ea49e8a7adec71062dc5df097be99d3975e92bc53a`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 28.2 MB (28245354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2900d390e81d9af67de96fc8c0a46074dae5d79691899bb1c249eff04d790cf6`  
		Last Modified: Tue, 03 Jun 2025 09:02:08 GMT  
		Size: 138.5 MB (138492458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4363836e3e3009d0549dbecfd01ff4316e1d5a6be1ddc468f0fed52270b5e83e`  
		Last Modified: Tue, 03 Jun 2025 09:24:22 GMT  
		Size: 73.3 MB (73291039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c0ffd536ea4bc8f0ccfb51bfa5093e38861c104515ead8edee98c6bd77d394`  
		Last Modified: Tue, 03 Jun 2025 09:24:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8428af2edff4058dacd0ac349f18a93887f4e7631c830e3d60a1c7ed18f8c13a`  
		Last Modified: Tue, 03 Jun 2025 09:24:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5f5149a61f724d2825ec1b59d06bdc34e4d979a76fedbc096666cfd0c8d1f006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5115513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6acbf60ad5d1b40457da481053c897abf6577ad3a3d298be43d98d38317402`

```dockerfile
```

-	Layers:
	-	`sha256:12fe64f0defc7345fd684aa93b6f9aac2be4b7904309c64b66300ee84e4e7a11`  
		Last Modified: Tue, 03 Jun 2025 15:37:19 GMT  
		Size: 5.1 MB (5099610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6598072ed9dfb9511ede6025b06f6d9ff838ab44f5e2af186385c0e215bc659a`  
		Last Modified: Tue, 03 Jun 2025 15:37:20 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e36abd0902bcccd0c7dfde8a75438c21224ecd90e4c200d1975cb6b8c64760d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239910624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c709d486010e1fd2deda50f075bbdc52f055890588c93b02455ab15a7b2314`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
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
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Tue, 03 Jun 2025 13:43:57 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89149c8ddf2f34bc00802d5cec3d426d775f8368fa79ab5455c34c0ba8a1e25f`  
		Last Modified: Tue, 03 Jun 2025 06:17:33 GMT  
		Size: 134.7 MB (134673567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a658ca803401700d6c026ca6f99a794d81540b2dec6e61d119a6421d7886614`  
		Last Modified: Tue, 03 Jun 2025 06:23:21 GMT  
		Size: 75.4 MB (75406399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5472fc27707c53beade6ce8fdf6a3fe948d7c3375095a2156dc3a3a5debc96`  
		Last Modified: Tue, 03 Jun 2025 06:23:20 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad09d59048c28baaaae7e8a8684c5c2ac55bd62b8881ac8354d730d88905a55c`  
		Last Modified: Tue, 03 Jun 2025 06:23:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e5e1b85eb288794f2b9dc227a7bfd17127ea973592ac09d9f619fd410bf23da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac7403aa8d7eec451715aa2d1ada3a9a6c4024d9cd6281ecf9b1c4e910e5e9f`

```dockerfile
```

-	Layers:
	-	`sha256:3f495135b786cee7ab9d1a1c2dd1d68c5a837533951c420e94c7d8d08828bc7e`  
		Last Modified: Tue, 03 Jun 2025 15:37:26 GMT  
		Size: 5.1 MB (5107989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e4b55ecf29ec239946cac36e79749e71bff9e85d1dada15aaf132ec9f2e46b`  
		Last Modified: Tue, 03 Jun 2025 15:37:27 GMT  
		Size: 15.9 KB (15853 bytes)  
		MIME: application/vnd.in-toto+json
