## `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:aeb782d91fb6ef0c69cdfe4ecc4dc13e9707714744515c70d9949f2790ebd9aa
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:83145431e62f610110bf1ef985077c4a16d794314a2b36ef3453c6ba8e9c2fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243841784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2332527911e769b4e7bbb5a6fb14d1747e77d701f48638e455102fea37aee66`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:17:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:17:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:17:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:17:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:17:16 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:17:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:17:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:17:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:17:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:17:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a60f39ff6be99994f165c3882b747e82a4d49d39b38145c6734a6dc21a2bcab`  
		Last Modified: Fri, 08 May 2026 20:17:53 GMT  
		Size: 145.9 MB (145905474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5053b3e62f481deae59764478bfceb7480d0829f1b1f00330f48d65983ee8926`  
		Last Modified: Fri, 08 May 2026 20:17:52 GMT  
		Size: 69.7 MB (69698985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23250a6a7ab35776454cffeaeda005fd6ade78bdc160ae69c8ee3b901d806450`  
		Last Modified: Fri, 08 May 2026 20:17:49 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1056bb8c245a3a096cfbe40a048e02b86119032e81a8c8fc801bd9c8458c85b4`  
		Last Modified: Fri, 08 May 2026 20:17:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8be2da884442a56be2d2715751186951fd5716b33244edb881f46e4839db66ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd1e0d6f4d328142c9cfe31ecb6d5b2b4c5c43940dfc6e5203cdb4940b72070`

```dockerfile
```

-	Layers:
	-	`sha256:5448cb98feeb5f7174ae7b01a73512230fbdaf382d4b255eb1d030c24afb17b6`  
		Last Modified: Fri, 08 May 2026 20:17:49 GMT  
		Size: 5.1 MB (5116794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdb2a06ea75551c4a4ccc3f5434c1d6e296cd413e723e9a5a17f2e770f2f6033`  
		Last Modified: Fri, 08 May 2026 20:17:48 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:98fe1b0640bcbafc7bf4af0323e3878b0a3362f8119c68b60d381c83e0deafce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242534272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d3762cf53b9e7d540cef79526ba06f596ed470c0c90a806c80390297fa7053`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:21:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:21:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:21:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:21:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:21:30 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:21:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:21:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:21:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:21:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:21:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76c21dcfaa3802fdb29cf8b60892ca6624564e4f90e8be0e58f9164e36f45eb`  
		Last Modified: Fri, 08 May 2026 20:22:09 GMT  
		Size: 144.7 MB (144724335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0863f41c7fc4c1fedb69a0425ea34df7e95839805c12b30e0a10d9099c7b1013`  
		Last Modified: Fri, 08 May 2026 20:22:06 GMT  
		Size: 69.7 MB (69692729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38753467222ed39974997340b224032603366d41cb286b6b477e42eeef8ea6c4`  
		Last Modified: Fri, 08 May 2026 20:22:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4561ddf15894f465a2fdaa809f22bcca13de68d11bf0abe60358dbf627efc377`  
		Last Modified: Fri, 08 May 2026 20:22:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:268e155c252abceab6cfa0956e97683121fa9b90460bb59493ee2bfeb8ecdd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7008cc7ee955bd18f583d07b653fa27fc7737259ec6a66f70fc059fbee9ffc`

```dockerfile
```

-	Layers:
	-	`sha256:33fd2d491e3eb32663c1721d34226dbb74540fa7d66151fc0476e7769fecf5fb`  
		Last Modified: Fri, 08 May 2026 20:22:03 GMT  
		Size: 5.1 MB (5122555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e970edacc17da9d7a6e2f01e2589de30ac30c3b95f2ddd14f59e730b040fb1d`  
		Last Modified: Fri, 08 May 2026 20:22:03 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:dbde8ea29d2613f0aa6eb3b1270ffc5a6eb9b5eafee6abcb792ce802da0656d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253375384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afd4cb34da6ad202940de56a4885f69c9b89252afe1bdc192a113937ee8a73e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:30:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:30:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:30:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:30:41 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 09 May 2026 02:30:42 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:33:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 09 May 2026 02:33:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 09 May 2026 02:34:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:34:00 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:34:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebb50b599e2de909acaf0c0d8a3d5a70b8d0e3b34206b32960ca5e3061a8a17`  
		Last Modified: Sat, 09 May 2026 02:31:50 GMT  
		Size: 145.8 MB (145766111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae26f59d818dee16bb130240b16dc8cc418072d43069ab061ab6dcd17779542`  
		Last Modified: Sat, 09 May 2026 02:34:32 GMT  
		Size: 75.5 MB (75529778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e282f6b28d434cb153133a004db6bc810690d643ddeceb1293eb2096226a306`  
		Last Modified: Sat, 09 May 2026 02:34:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42b5abae842f5ebd092eb2f527a84c49aded9b817bff3b631c9316537d96d2e`  
		Last Modified: Sat, 09 May 2026 02:34:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e0deaf41592ebf9cf710e259e1831e7eb2527962decfa12b08959ba71bf13bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ff5a6d000bb03790e9000b0f78a6ef965215c98614e17d67364280d3d1a2a6`

```dockerfile
```

-	Layers:
	-	`sha256:d0c07199e32ff7f8b209e0e459f1ac071cc576876377692633f4ae1a8945dcaa`  
		Last Modified: Sat, 09 May 2026 02:34:30 GMT  
		Size: 5.1 MB (5121952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0d2163c31b6222ee911569b3908feabfc60598df49c40ce112d5575f3ca3f7`  
		Last Modified: Sat, 09 May 2026 02:34:30 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:51be603fd4d4794c8dcfc71a5051a85d2e681a66a05aad4734d2b171dfcf645b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231315901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4d5a6d05e5eeed77751844949e4e696406ac8de4e03a1fa17739b01c1147d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:14:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:14:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:14:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:14:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:14:57 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:16:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:16:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:16:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:16:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:16:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c10a6897782f771d3606e3e80b8e1017d240690fd955802892aea8e434131f`  
		Last Modified: Fri, 08 May 2026 22:15:37 GMT  
		Size: 135.9 MB (135910446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccf1ce2424ffa5f8713172acbe828323e7967a679974841473c16862cc5dcc3`  
		Last Modified: Fri, 08 May 2026 22:16:34 GMT  
		Size: 68.5 MB (68512811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c905fc8c40592c5d4cc6e2e6cab0668dc5fbdd99d3ab681ffd846533fd1f0644`  
		Last Modified: Fri, 08 May 2026 22:16:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fb636bf4bfee053031c578c0ddeb23c58a2e043d82a1b54c333cfee417c1d1`  
		Last Modified: Fri, 08 May 2026 22:16:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:badea48bc191f65471c04cf5371ceeecbb6153f585fe1b472183baf09997b122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5124105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727bd580bcf83dd777fafe2c28c83a9cc1ab3ad137143fb01dba110b437ba30e`

```dockerfile
```

-	Layers:
	-	`sha256:98a79a2e509a85529b2720dd1c7efd5e4b9b9f0bf95cefd2669ef3171332f68f`  
		Last Modified: Fri, 08 May 2026 22:16:33 GMT  
		Size: 5.1 MB (5108115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7215cff850f84a45dd72d67da71495611181eb0213738c51ce431bdcb3d18402`  
		Last Modified: Fri, 08 May 2026 22:16:33 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
