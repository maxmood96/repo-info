## `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:bfc86e08abd74461848b8f4e3fb05abf4154dab9d4a9ad5c6410a40f9e05e4dd
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

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f559e5d949046483d7cf02bb8665c5c3a9520e55988badc90c90a034f1315e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192392149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4d8e3effe73b2b64b32b688189a4a0621de83e4e5629fec2760778abb38010`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:20:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:23 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:20:23 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:20:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:20:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:20:37 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:20:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3f092abaf117f3902ff5203a074f97f97277b79fa912082a53f212ed499cba`  
		Last Modified: Fri, 08 May 2026 20:20:58 GMT  
		Size: 94.5 MB (94455697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce40ce19bdac79c6332e8ca07607d049ece211b4357c75cace1906715e9c4d1`  
		Last Modified: Fri, 08 May 2026 20:20:58 GMT  
		Size: 69.7 MB (69699127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269cc42d1f02ccb208435e1dd56d852f03d7d9534b8b46e923cfc778a62df25f`  
		Last Modified: Fri, 08 May 2026 20:20:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e236567fcb9953bfb466f3dae5a75a6fd10be927c40fd6b2f9a7166d6dcd65`  
		Last Modified: Fri, 08 May 2026 20:20:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb020f342ae1f333790f92943cf64e32989b670b10cd2da82c2db4e3045e39b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e455f8743084d575162b5f10ff296c562f352d5cbd6b7818f035c1546d333c38`

```dockerfile
```

-	Layers:
	-	`sha256:9ee94180679786550d4aab326c5baa5eef1b458c2255b1e1b3681665c0b09d74`  
		Last Modified: Fri, 08 May 2026 20:20:55 GMT  
		Size: 5.1 MB (5081671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62661838b2481578c118977bb03de1da23d65a67aadd933dd5c6b2b62267ee1`  
		Last Modified: Fri, 08 May 2026 20:20:55 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:55429e2a0c14945131fcac0838572a434106a7a2043057360e8530beaa48d67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191204948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afed5d5a638a087410f76b88f653bbd8a01f523d97cfd69ea805e05db2d683c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:24:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:24:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:24:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:24:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:24:58 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:25:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:25:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:25:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:25:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:25:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b607a2a443e557c241a2c8ce9dbb867f767ef4b9c723c3d6e0526c469198c28`  
		Last Modified: Fri, 08 May 2026 20:25:35 GMT  
		Size: 93.4 MB (93395166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1d11d72e4c8d671465c77c54526d1895ee432f136c8fb3e35cf2180053a74e`  
		Last Modified: Fri, 08 May 2026 20:25:35 GMT  
		Size: 69.7 MB (69692575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90e5aea1e664fcb3c794006911191d91384e658269c8abec6a814249b939e38`  
		Last Modified: Fri, 08 May 2026 20:25:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3584a1d6b55c18453bbff4ad13fb270f7a1ad743ac127587cf678828c1d736`  
		Last Modified: Fri, 08 May 2026 20:25:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:35727bd4cac5cff7ee36d7994007d41ad77ccd0a12faeaf720b97af715c5d35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5103374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2405586edaf3c96bd5c3145cec3978fb448388f3638749423af85944852e56d5`

```dockerfile
```

-	Layers:
	-	`sha256:6c26ca703481a1ee80e142eda0abe3ee75e8df707f8e062ca041ab776681812a`  
		Last Modified: Fri, 08 May 2026 20:25:32 GMT  
		Size: 5.1 MB (5087429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fa626b3a5ede723e8b95f9879e4a0f378766149a305c8c5491c7d3aa965bf64`  
		Last Modified: Fri, 08 May 2026 20:25:32 GMT  
		Size: 15.9 KB (15945 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0481d3ede7bd2109e7e024807ccad6f00db228c1657af91a2b8f997ccabefef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201390800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5648016cd3a4437fdb66f4ee8736ae204359fa62510f63117916e6a6d97cd7a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:47:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:47:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:47:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:47:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 09 May 2026 02:47:26 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:50:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 09 May 2026 02:50:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 09 May 2026 02:50:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:50:33 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:50:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea74e2d5f082a4e3bed610cad5118f31172b96baa2083e47ff5cde42b672f30`  
		Last Modified: Sat, 09 May 2026 02:48:28 GMT  
		Size: 93.8 MB (93781494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717bfd987ddb12c13b1b02d13ed6e331f77f6fc66cd174cd9012c0db6df6aa56`  
		Last Modified: Sat, 09 May 2026 02:51:06 GMT  
		Size: 75.5 MB (75529812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24742fe7369710c084e92bf5eb24d696040763b0a1d177f99db7b8ff8d962a77`  
		Last Modified: Sat, 09 May 2026 02:51:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e018f7cd0d5e8432ed5b52f5f77fb945608d1c793bb68be60fca232811c734f`  
		Last Modified: Sat, 09 May 2026 02:51:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:db36515b38b91a96a5b755ccc3c45750ecf83037ee8bed31fe42d8ed5bf193df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b25763f7cf50bb80743b0fe92f03d03ee3ebf2cf990d3187f8c3cde73056271`

```dockerfile
```

-	Layers:
	-	`sha256:64a7fe3d929836df4f17754f64b0ce8e5f2c31a7993084f1727aa21d12ff4e00`  
		Last Modified: Sat, 09 May 2026 02:51:04 GMT  
		Size: 5.1 MB (5070765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a09e14778e394552b22babcace0f2bd51e54ee53c5467da3f39aa36c72b2d6b2`  
		Last Modified: Sat, 09 May 2026 02:51:03 GMT  
		Size: 15.9 KB (15877 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:93891f503329a6b90346b53411291499d5a1376f400728d0f1550efc5bed4b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (185954493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd5c32792549712f29194097d6c532f3b0249e8272b89f3f8cd538476969923`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:20:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:20:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:20:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:20:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:20:51 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:22:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:22:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:22:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:22:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:22:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b107cb0db7a1b32111d505e036bd5a5247c7ca1efbd8c49045017953aefc87`  
		Last Modified: Fri, 08 May 2026 22:21:30 GMT  
		Size: 90.5 MB (90547730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e4aca1aa8b00e9f613b19e4af86ab6698212e5d2c437e4753e1f3c8d3bcf54`  
		Last Modified: Fri, 08 May 2026 22:22:24 GMT  
		Size: 68.5 MB (68514115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c80b6abe882d12e5250c793d0a27df42dd965d2481ba5ad2005130f0b060fa`  
		Last Modified: Fri, 08 May 2026 22:22:22 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d2fb8bf5debd6efc9083543037a02cc8ee88a181c9fca92c93c94ca77c711c`  
		Last Modified: Fri, 08 May 2026 22:22:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:857f8d870988b0244b2871da88d2df7c0fae45bab21da902a6c76f7778c4521f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324497c1e091bd47b049ae4dcd00ba4bb0bbdbd2866a46fe9ce1b855bb7bc08a`

```dockerfile
```

-	Layers:
	-	`sha256:ee4e149bc4629b436824b96083a6b38577d70a4e625a69be1650a7c23bc4836a`  
		Last Modified: Fri, 08 May 2026 22:22:22 GMT  
		Size: 5.1 MB (5058178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84800a112df616378fe4fb25f7109d1c053553418bc431abdfcd0321e137cb6b`  
		Last Modified: Fri, 08 May 2026 22:22:22 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json
