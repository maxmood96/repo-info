## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:c1a134fe61075a7809c0090cb268df9c65c5f2aaf3e1879bed6b549363377e89
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
$ docker pull clojure@sha256:4b25e90aaad8cf014706ed7b75c3830f4e1ba2f0b937cdb1d0450050b6f47c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247403547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dba105db611c66952e6330179d20ca0e765800e1d9ad4efae8e6c1da783bb8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:04:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:04:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:04:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:04:54 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:04:54 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:05:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:05:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:05:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:05:10 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:05:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc8e19eec260fe634438bb83a7c2ba88c3635c1f7d170b3c2083343bc8a23cd`  
		Last Modified: Thu, 05 Feb 2026 23:05:31 GMT  
		Size: 145.6 MB (145628508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8addceb84719547c0264bb0198ddfefd09d7aa1b3a3d5046884d8ceed5b3b512`  
		Last Modified: Thu, 05 Feb 2026 23:05:29 GMT  
		Size: 72.0 MB (71995401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4ff800bf321b863a2cd201a5e7fb2112908421ed8623295a4cbe9cc1ff989d`  
		Last Modified: Thu, 05 Feb 2026 23:05:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a9040f37cb65e367401c88f7347eb01f29b6371d96e17e66beda9ad4a55660`  
		Last Modified: Thu, 05 Feb 2026 23:05:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:083758e80f670f5fe2b7306d5c0696e9146f5e8584c30e593d48af08636c5aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24f69e03a802aaad7331c1bdfb31d27f4f1bb779877d736052ebd542df020b5`

```dockerfile
```

-	Layers:
	-	`sha256:5de4df408e9deae8097522d347b5196bd2af1d974f8796b3a53056e28f14b2ff`  
		Last Modified: Thu, 05 Feb 2026 23:05:27 GMT  
		Size: 5.3 MB (5257551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd868f6dedc0448c0ffb16a8054645af1123cec9ab4e4ae2efb073bbc6be59c`  
		Last Modified: Thu, 05 Feb 2026 23:05:26 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:94558e6b67a84a9c4b208cfd2c34b634833898f5e4ad896f9375481aed758b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246383906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e21f1ef857f74de99f4a91bc9d7fb835ca7df9fbd9a98f29f59f74a770b697d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:06:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:06:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:06:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:06:22 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:06:23 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:06:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:06:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:06:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:06:41 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:06:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef7b8974468684a689b6915787d589a5a41c7b43492c3769d1c6569ddd2d193`  
		Last Modified: Thu, 05 Feb 2026 23:07:05 GMT  
		Size: 144.4 MB (144436235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27189008e8d798005a7372d9067ac05a9a7934d9c88ac61b90e7553c2169120e`  
		Last Modified: Thu, 05 Feb 2026 23:07:04 GMT  
		Size: 71.8 MB (71806563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccd22626109659393542dfcb805b41e700393c77d5d015df09eeb70bb0dad21`  
		Last Modified: Thu, 05 Feb 2026 23:07:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac551ae3e3734dc24810d1b98aba843cf237d51aaa58ca0a3fac4f4e3a3ad79`  
		Last Modified: Thu, 05 Feb 2026 23:07:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae344a74baebb03f0c105b243e47106d2eac01e2482ea678b53daf4494a8e7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fd1353a9e258173e9e7f5558a99d94fd670a1d1743e617d62c1ee2482ce099`

```dockerfile
```

-	Layers:
	-	`sha256:df75f64fafaba97f40c8c37edd650fc3ce68ad27f32e0392dd0b207bc732b170`  
		Last Modified: Thu, 05 Feb 2026 23:07:01 GMT  
		Size: 5.3 MB (5263320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967925f10faa440363f6f5719d5f20d1a7241cbf3dbef9d85bffe53a42fbfa98`  
		Last Modified: Thu, 05 Feb 2026 23:07:01 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:abbfe06c54dff10a51b0408096100e1b55a21b75e73ef4a9029caca3b19b29b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256429881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd864fe5696f713f00fbedf9bbbf8ff25f08adc1f01af4bd6127ac7121fc97e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:25:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:25:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:25:39 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:25:39 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:32:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:32:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:32:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:32:52 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:32:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806148462c30ed1bfef62eebe515a501af99978464a4710c612e54794c9190dc`  
		Last Modified: Fri, 06 Feb 2026 00:27:41 GMT  
		Size: 145.4 MB (145438280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98487951ac4bc2c715fb3a90afb8dbce0526938a979bfe906080c5e2a7c2ce6f`  
		Last Modified: Fri, 06 Feb 2026 00:33:39 GMT  
		Size: 77.4 MB (77390376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861f7a4bc63242979f9837e5153c2b2b2112983b766e97692e975dbe8f1d5968`  
		Last Modified: Fri, 06 Feb 2026 00:33:36 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6630d7a0a5063957f0e08aa33a2c9dbd548d96f7234b4038196cb67b7dd7a5`  
		Last Modified: Fri, 06 Feb 2026 00:33:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0403b2bfc3017739928e66efc4ce0974710483d03e49fe6f4f63007d24c09264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0da7de586c452dc3481a242975843f28557e3c9281d9cdb2236191b8315bea8`

```dockerfile
```

-	Layers:
	-	`sha256:11d8eb5c57b5ec8c3cdcf61a58cb356801212571a6cbfee92710469877a6d611`  
		Last Modified: Fri, 06 Feb 2026 00:33:36 GMT  
		Size: 5.3 MB (5261922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:887b1e053490263de49f4a511bd53a2cfa9fe4a9291c07373209502e8f727722`  
		Last Modified: Fri, 06 Feb 2026 00:33:36 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:f4ef81d85dbb59413eee11c8bdd711e62f35bd8f407694393f1be0920dccbe78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241046164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c99d33386092315ef16bd54fab740a2facad06929e77b8555103266df68d304`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 20:21:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 20:21:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 20:21:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 20:21:12 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 20:21:12 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 20:38:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 20:38:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 20:38:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 20:38:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 20:38:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37b86b79863af50599316c3a3436311cf8411ecea8381a02bba71598ef65c4b`  
		Last Modified: Thu, 05 Feb 2026 20:27:16 GMT  
		Size: 141.9 MB (141889583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bf43e298e4ccd5a7b53a8e400aa6581ce4b153aa423fdd6b95ef78992f7a5e`  
		Last Modified: Thu, 05 Feb 2026 20:41:46 GMT  
		Size: 70.9 MB (70879147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40f623b10483648312fbf51e435c8680b9d3ef7f6e93d379afcbd505549629f`  
		Last Modified: Thu, 05 Feb 2026 20:41:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7bee8f9c1f1f67c14d0800e81f32677d4b81d0a09790fcd610426b3abce540`  
		Last Modified: Thu, 05 Feb 2026 20:41:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6250edd7c7539e0c4abeeb1b0bdce279fb8f81a491b27dcd377f2cc22d8fd432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303e54791f0f617adedbdd8b533a4f84e8b13311bcff76b95ee9a3efbc49f523`

```dockerfile
```

-	Layers:
	-	`sha256:c1ab79426c257edc36fe88492c1bec614f67fa346e470a3e95c5d965ebea2736`  
		Last Modified: Thu, 05 Feb 2026 20:41:36 GMT  
		Size: 5.2 MB (5243844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea98f7dbd0ac6c689edd1d68d4a3438eeb324086fbf8be743e71343ca075740`  
		Last Modified: Thu, 05 Feb 2026 20:41:35 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:7692eb18132417fb28230302ba322532fadc884c2153ddb4bf3b7e5a783125c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238419110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c746db211ad7253f780ae293a051c8026a83a255062306b2985bf19e6d13996`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:04:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:04:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:04:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:04:57 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:04:57 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:05:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:05:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:05:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:05:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:05:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93d9217a8722bf1575b25697aa59ca55388f0c47c3f649322398b3a70f4c8b2`  
		Last Modified: Thu, 05 Feb 2026 23:05:43 GMT  
		Size: 135.6 MB (135627061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4765376ecab37b294d36bdce3d93f6ef82961601992da4ccbb47b86b25d0ef6b`  
		Last Modified: Thu, 05 Feb 2026 23:05:42 GMT  
		Size: 73.0 MB (72952859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4c25a224c6cdc1aac75995b7e148a598a90ddec972a33dca2387be3e53c77d`  
		Last Modified: Thu, 05 Feb 2026 23:05:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244d56e5b19a2fb77c5ca62a097f06c9e4ca5ad0befb9eb9b3d1fbd81cfb4df7`  
		Last Modified: Thu, 05 Feb 2026 23:05:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f6dd0d9811066ac04c92ab158be8309c617370cb15d1d68c2a534e3cb59d227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36a796a25eadfde5d645f70ec6b0aaa09dae4a418c24f00d4f41f66f046af25`

```dockerfile
```

-	Layers:
	-	`sha256:6c5b31fceff859497866c28af84dfc1661068c826d30fef478961d5765741caa`  
		Last Modified: Thu, 05 Feb 2026 23:05:40 GMT  
		Size: 5.3 MB (5253475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b6b525721c32a202800dceac60fdbee5c0b98b688821ac1f32c5fcd5e040e75`  
		Last Modified: Thu, 05 Feb 2026 23:05:40 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
