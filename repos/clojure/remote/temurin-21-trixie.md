## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:4a225366eb72b71f6a3e69f81d22f92903b46dcd02b6afafde62dab05692f7d0
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

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:09a21d8d19a403177c735c4050a32cdf86f26b675139da0590b73fa4bb05c9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292730924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4dcf609af8a923fc3a1f78d68fa78bd932bc2760d2f9d82f0422bbb939e38e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:50 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:20:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:20:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749ac892fcd735f7c2e252e553e8148e3b4a4b6b2c2bf149b8d33e8fe92efaee`  
		Last Modified: Wed, 22 Apr 2026 02:20:31 GMT  
		Size: 157.9 MB (157857054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa1edbc2b925b6566eb08ed75e546d8bfcf8d02bf12c16561e6680a01c39c3f`  
		Last Modified: Wed, 22 Apr 2026 02:20:29 GMT  
		Size: 85.6 MB (85570731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52d25635c3ccc35947ea7d0a4f0b030271a82fc514b163d7e1c8d53d7dcce42`  
		Last Modified: Wed, 22 Apr 2026 02:20:25 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb9a5e1f7e11b30a6685f7072acd72d01ffcfcc6b61197cab256ed77b6cb442`  
		Last Modified: Wed, 22 Apr 2026 02:20:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e930d1d5f94c489fd3ff36b2e95748555fb105a8e4742a860bd23235f42214e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212a82e9e11bd6294cec0f36afef985f3cfa6adeea2221e4ca09c801eb06d4db`

```dockerfile
```

-	Layers:
	-	`sha256:fa514e99b7a0c6e51d0fa5141870ab083d3b40a30a2d7deb0aaa56165b23d349`  
		Last Modified: Wed, 22 Apr 2026 02:20:26 GMT  
		Size: 7.5 MB (7472573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20ffe026e4604e4dbb010618dda297a10fd0b10615fb32dd0a51b9ff4daa6f14`  
		Last Modified: Wed, 22 Apr 2026 02:20:25 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9966d01ad3055d4a48078e008af36fe4d2964e3fd0b90feca1869b5a73be9178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291186745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71e455d4ecb594cfed9027437a6a94bf95af1afe4234571ccd475d7bfbb3f8a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:23:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:23:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:23:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:23:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:23:31 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:23:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:23:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:23:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:23:50 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:23:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b2594b313d306b3ad2ef11e5b022a8281a79dadd45b5e4d2bb93c14d42c24a`  
		Last Modified: Wed, 22 Apr 2026 02:24:15 GMT  
		Size: 156.1 MB (156133076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7470172a3521add5555a7f2e19b0911f4e6e652c9aad7e478a408f54cd24b869`  
		Last Modified: Wed, 22 Apr 2026 02:24:14 GMT  
		Size: 85.4 MB (85383383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54a9aa328396d8df45e63e74b7f7469cb78e208b3c4803c96b817afc77fbef3`  
		Last Modified: Wed, 22 Apr 2026 02:24:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ca8c6da05d56adaf709e409a722a32fd6d45aab32caf316a11fff9deb8d206`  
		Last Modified: Wed, 22 Apr 2026 02:24:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a41c04b32c01566deca905cb8f449a59eafab3a639e700a40565b85b9e163117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7495475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b9ac2530bb83a3728ffc6b8e0445342e7e272bb01e53cf8e60cf2051ccc54b`

```dockerfile
```

-	Layers:
	-	`sha256:c763fcd5114f16fa06b1659fbbe5c1c421e73adcec09267f2ce71042587129af`  
		Last Modified: Wed, 22 Apr 2026 02:24:11 GMT  
		Size: 7.5 MB (7479603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e25cfe7811ca762a7d3a63f75b84f1a0c03142eb68ea974b0f284d4ac95aea`  
		Last Modified: Wed, 22 Apr 2026 02:24:11 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8a076f27b06ebc7c1546919c41e2de066336658c48dd85ba3c1a75b7b65a787b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302087854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3aea2113b7e73f6057b80022a946a20e86eb03fec511430d3fcc425b99c822`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:39:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:39:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:39:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:39:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:39:30 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:43:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:43:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:43:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:43:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:43:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfd4a596860411869ba1b27f063b5f93a5f8477634fb7f87b5eea1fe9858af2`  
		Last Modified: Wed, 22 Apr 2026 08:41:02 GMT  
		Size: 158.0 MB (157977486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475e9f3be26e1181e8a4583bd1bcca4efd24f2f84fc3fe1d5145183333f56dba`  
		Last Modified: Wed, 22 Apr 2026 08:44:38 GMT  
		Size: 91.0 MB (90986344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a160a8a5fcf2e9c148d82f3d8c1a0164cda0aab0b4760712ca8b886781495f7`  
		Last Modified: Wed, 22 Apr 2026 08:44:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c33d320fbc9e5ba8cc07bdd9c88f38b62d6fe20d4b49b120cfe04453a0675c`  
		Last Modified: Wed, 22 Apr 2026 08:44:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9e1cbc104615e30da1638557f2a840a880ae09abd7663e64ad484c9e31236e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600a7103fec5579e8224acea5d808949809a4032252aae074fb086cc719963e3`

```dockerfile
```

-	Layers:
	-	`sha256:0d34353b6f483a21512984472633e8bf17f85f72a13946674ccad016c4f60ab0`  
		Last Modified: Wed, 22 Apr 2026 08:44:36 GMT  
		Size: 7.5 MB (7476994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1f0a98b1e399b59a5fa9e193c38c2a89e365f46385770ac8d374e49123ad480`  
		Last Modified: Wed, 22 Apr 2026 08:44:35 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:80eaad3fd1b7f384b3d5bae18b3bb8722f24fd26e5021dcd6c6780a33b638cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292641518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6300eda46c9d29be975d243e856e6c76110aac28219074ba804e3112cb6e0c30`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 21:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 21:53:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 21:53:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 21:53:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 18 Apr 2026 04:44:33 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 05:03:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 18 Apr 2026 05:03:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 18 Apr 2026 05:03:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 05:03:41 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 05:03:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2e07983918932b6a7d3f5b469a0f96350899d0eb2de01a34ca1ec47825c8ec`  
		Last Modified: Sat, 11 Apr 2026 22:00:22 GMT  
		Size: 157.2 MB (157216895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9348d5aeb66ecbbcb20ef5917cbaff965e39251a8674586ae79e10571a345dc`  
		Last Modified: Sat, 18 Apr 2026 05:08:13 GMT  
		Size: 87.6 MB (87630951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fc236bc14fc77a559e91882a2454876eaee5e2300890d193aa7c2480fb4fcb`  
		Last Modified: Sat, 18 Apr 2026 05:07:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480bc1ddfdab578d1d90af9b20a05602c869b156e0eafac0925e211116b42251`  
		Last Modified: Sat, 18 Apr 2026 05:07:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8c936cde34f4feed420ccd501432e7b0983e29ecbb464426e7e5f62877b56281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7476236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0292a15fdfc192966f9032b774ea35e7890aac657789f0f7859273c3f3f81ed2`

```dockerfile
```

-	Layers:
	-	`sha256:0bea7c7e3ab2c4582579e277ffb99e91119eced58461641c6b9a1dd3822860df`  
		Last Modified: Sat, 18 Apr 2026 05:08:01 GMT  
		Size: 7.5 MB (7460434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:912e66acd61e032a6b4df254347fca0584fd17cb7ddec02d9cbc37a035933120`  
		Last Modified: Sat, 18 Apr 2026 05:07:59 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:af763a523e13486c9f1622989f05dc6b884a6aa22c4e1ec4818d0eb5320209c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (283023392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2ff871b78f1a5c677d5847996380e43aff685dfbef5548a42cb79fe76db80e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:03:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:03:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:03:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:03:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:03:12 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:04:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:04:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:04:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:04:30 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:04:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cdd84aff24f59863daaed198419b0074a2a76183e68980d9cedc370030291a`  
		Last Modified: Wed, 22 Apr 2026 04:03:54 GMT  
		Size: 147.1 MB (147105212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe6b92bd2e9abef5d9e28ab9dcf1821d33eca057cee3ea6cdea475fec82bb3b`  
		Last Modified: Wed, 22 Apr 2026 04:05:02 GMT  
		Size: 86.5 MB (86545033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ad677bae19aa35b2c03531d0e7781838e0fe0a52a68ef8e55a241adedb20e9`  
		Last Modified: Wed, 22 Apr 2026 04:04:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56171ac7de425ce14089e3f3da0c83a3b7bcfe1919ceeb2fd81074543d86d907`  
		Last Modified: Wed, 22 Apr 2026 04:04:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fe6ed8757d8c334e827eb9c39c5d6e7f7e5ce3f17423793b786898ed4c1a1a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bdd5ca69b83be9d7e56b65dcb27314445072c5415fb519075372b3f4ee72b7`

```dockerfile
```

-	Layers:
	-	`sha256:c3c5616689fb48df60651d5230294fe485665fc6afd025870b0b93b5a4f01d69`  
		Last Modified: Wed, 22 Apr 2026 04:04:56 GMT  
		Size: 7.5 MB (7468495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da53ddeeac82044b8acd19d32c59da38e64013b132638481b120f866a769ceb`  
		Last Modified: Wed, 22 Apr 2026 04:04:56 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json
