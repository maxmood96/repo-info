## `clojure:temurin-21-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:e863aef2e55c68884f3ae3ee342a5cb01ac23b652ecc6252687d8b893b5ed65a
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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - linux; amd64

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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:59e31c73513f119ee431c54503a0d8b11bdfd586f3611d43e6c18f4da6524c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305819264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c600f3ea9e955c6d3c08e1fe9827200f5ea45912bcef2df9d4ead8926d84eb09`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 03:01:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 03:01:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 03:01:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 03:01:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 03:01:40 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:07:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 03:07:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 03:07:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:07:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:07:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5605a6e452c48331997194aeebeaa58faccfc0cd45ba29af35316c69a1fefd`  
		Last Modified: Thu, 16 Apr 2026 03:03:21 GMT  
		Size: 158.0 MB (157977558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccdfbab45476b6830016a629408cef747ae4f3c54bdc2811fba7d1468907619`  
		Last Modified: Thu, 16 Apr 2026 03:08:17 GMT  
		Size: 94.7 MB (94721995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af2d35b02fbb3bcca2b6e61d35db3fcb02cb586d86b57762bf5cfb109e430f4`  
		Last Modified: Thu, 16 Apr 2026 03:08:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8af850d5443a0338022924395fdfc39c35122234960853f8002e58948e9ace4`  
		Last Modified: Thu, 16 Apr 2026 03:08:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:13870b18edd5c572305ffd3a0605acf189b7ba585c86955b10d98ccd97286817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b061065a2b668fe4508a4abc6959d44916168dd059dd34751694c0075d352d0e`

```dockerfile
```

-	Layers:
	-	`sha256:6c42d55328b11a11c7026240f08091a86aa097f190c35ec66849728474ee0806`  
		Last Modified: Thu, 16 Apr 2026 03:08:15 GMT  
		Size: 7.5 MB (7476940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53940cce0e3a8e66dcc07739e67aa8d3bc160552cf3f31cd8ff4f7e84993f9ed`  
		Last Modified: Thu, 16 Apr 2026 03:08:14 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - linux; riscv64

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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ebc37b4ddf9db9ba0363c64317335b8ff336c5ae6142f7e732452eb90c0c0c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286181774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9ae2472d64addf7c807c1eabea1cae47e91643e811c01b85d575ba4da015ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:41:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:41:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:41:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:41:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:41:46 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:43:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:43:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:43:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:43:15 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:43:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e022bafa62bda64d6a51a016ec92ced7e9445747c5f54cb72881b028f644c812`  
		Last Modified: Thu, 16 Apr 2026 00:42:30 GMT  
		Size: 147.1 MB (147105267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d81c70890d0a7e62ee653e8f8d2b5882dac91b9a443de5cb1bc060e2aa90d68`  
		Last Modified: Thu, 16 Apr 2026 00:43:45 GMT  
		Size: 89.7 MB (89710361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce259bca5cb5427091d901e18a5ceb30b5782daab188414da3943a3ac887332b`  
		Last Modified: Thu, 16 Apr 2026 00:43:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0690b95bcf534561b46d33ae6140098999ee774de23f23b19084ac1cb4860c`  
		Last Modified: Thu, 16 Apr 2026 00:43:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8167dd000fd80c459677262c06a5d0712303836aba86bb2c489a68da2378c744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9becb20c839cd9423edff921dcb79ecb04acb1f084d039f773e28df1d11b8d`

```dockerfile
```

-	Layers:
	-	`sha256:28fbcd06a9fb0886ce42b17aa5e65b95ae7b71bc22327632fb5bfbc2245c7c20`  
		Last Modified: Thu, 16 Apr 2026 00:43:42 GMT  
		Size: 7.5 MB (7468441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da4362bcfc5c4fad6acd16365720b81cf1779d426b03ac8a1631d362907c670c`  
		Last Modified: Thu, 16 Apr 2026 00:43:42 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
