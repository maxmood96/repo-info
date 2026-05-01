## `clojure:temurin-25-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:abf48877ac3fbbc9686f20dabd4199a32df65c65ea75bf8e7655edc046c20f1a
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

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:28b8d6ea7069c450f59be3b45bad06940928324ef8380ea812cff5598783f2ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190510888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95b8f1f21ce875b225343fc2f8e7b4248716b82ac6b5fd38677dea663d1682c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:53:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:53:31 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:53:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:53:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412cd21a682004359d92bf4ab10cf2a9881286bc457907fb28d6e90fabf62de7`  
		Last Modified: Thu, 30 Apr 2026 23:54:06 GMT  
		Size: 92.6 MB (92574579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73db5e7aca4a0e98f3650e6f49da40bce93615687ef87887922ca058647fe82a`  
		Last Modified: Thu, 30 Apr 2026 23:54:05 GMT  
		Size: 69.7 MB (69699019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c725a08f475b66130614628b30ee8d7d138764544291fb870654d550c9bc7b5`  
		Last Modified: Thu, 30 Apr 2026 23:54:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94eecf1213e45d3e07ba518c1049fc31ad2caf2b55af2c9213f17f40079fc455`  
		Last Modified: Thu, 30 Apr 2026 23:54:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7a8c1a60012fd9164a353f1882696628be2d59594cb41fe5240d8e1a3c254a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5101407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed55fa9cb021d8b2cc74835d7d3cd0d5cafee77644a642a2381aa64783c57d4`

```dockerfile
```

-	Layers:
	-	`sha256:958533053eac9316267c15019c5f085f1f03c7815bf19ab2cc620a93d0da20e8`  
		Last Modified: Thu, 30 Apr 2026 23:54:02 GMT  
		Size: 5.1 MB (5084884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b9933668e176bf26662f8daa93cef665354cc6fcd2032a3db6b8b37376b6bce`  
		Last Modified: Thu, 30 Apr 2026 23:54:02 GMT  
		Size: 16.5 KB (16523 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bc2a679732a6507a15154d3de9785ae3f6be3e0645158fb9ccec77f33ed1d76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189351738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a63cd3f9d990085179ac6ae48c44fdc01380cb49cd804b00b25468f3971c732`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:53:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:13 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:53:13 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:53:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:53:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524efe48324acbc464db7fb037d9e0d717b2cff9542df61dec8af97d65f2e74f`  
		Last Modified: Thu, 30 Apr 2026 23:53:49 GMT  
		Size: 91.5 MB (91542247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d30c81e437a8e0e5a297019e5e3c005b25fc78bfe245e364db4b9a8624c784`  
		Last Modified: Thu, 30 Apr 2026 23:53:48 GMT  
		Size: 69.7 MB (69692340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26da8c3cc7956d97dc0b4845cbdaa802d4738d5065957b8feef8eeebc220888b`  
		Last Modified: Thu, 30 Apr 2026 23:53:45 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b711c981ae63ac8281b3defcc2a92ce845b2246d8903ef062de3beb86cb89800`  
		Last Modified: Thu, 30 Apr 2026 23:53:45 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:16a59e8f7925e6826c0cfccac11869bd51e8ebde96e6b13b779d0f37f3596db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5107332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e2222e5f76fcc5cf89ee64a20caabd8170ab268b12afedc9bde555d9d765c1`

```dockerfile
```

-	Layers:
	-	`sha256:eee8a3e224d3fe7dafb791db4ed78def236ad6fdbdcf2ec2e30256ee15725354`  
		Last Modified: Thu, 30 Apr 2026 23:53:45 GMT  
		Size: 5.1 MB (5090666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df23d1f7094d2b7a0261917821749d207ad88ec9aac2e1e8644ba8fc95e7d186`  
		Last Modified: Thu, 30 Apr 2026 23:53:45 GMT  
		Size: 16.7 KB (16666 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:aacdce532c6df40dfe0edec1945c5a7c1e4790dfb1dc33a355dd25d6f6a6e0b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199523631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbeacd80a6c74dc82cb67922c047a9f77fbe42d3f365fe8bdd662498f133b096`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 01 May 2026 00:08:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 00:08:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 00:08:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:08:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 01 May 2026 00:08:53 GMT
WORKDIR /tmp
# Fri, 01 May 2026 00:12:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 01 May 2026 00:12:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 01 May 2026 00:12:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 00:12:58 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 00:12:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b864cb58d14d804b69aef93f888801a5a40998b4ed809b787a8c67eb93313014`  
		Last Modified: Fri, 01 May 2026 00:10:07 GMT  
		Size: 91.9 MB (91914022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8786345af2db378e60c165e415a90d2698fbc1b959b3565d78778694de859bf7`  
		Last Modified: Fri, 01 May 2026 00:13:45 GMT  
		Size: 75.5 MB (75530162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59b1e8779b1b0a2c4e739d69e3b5f7dbbb2d1dff2cae0d9e125ba8ecf5aa269`  
		Last Modified: Fri, 01 May 2026 00:13:42 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e117e436df908b7c0b26305745b4520f81a4f9ef10d5254d8c3920560b9480a`  
		Last Modified: Fri, 01 May 2026 00:13:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd06625db85045a7c6ab0091050704b3f31c0223660dde0a99a21da8a78dcb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5089951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752f14b43f46c53818f60be94fd1e80929369d7bebb804ce24f3614ae2a045ba`

```dockerfile
```

-	Layers:
	-	`sha256:4b375ac096e409b61b55265f1ad962dee8ccd0687ca836298a12f4ca1348290d`  
		Last Modified: Fri, 01 May 2026 00:13:43 GMT  
		Size: 5.1 MB (5073366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc9a815e02cac6bffbb74721b1dbcfec88d235fc59c16fcce3805185a9e05ec3`  
		Last Modified: Fri, 01 May 2026 00:13:42 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8e0365d7e21985c1db9260c594336ded371c697395441c12d0dade603d8502ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183825911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30f23ac5e8b1bde2a1934139452c3640dee88b513c7d83b0c6ca4cb8c6e8253`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:50:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:50:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:50:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:50:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:50:05 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:51:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:51:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:51:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:51:31 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:51:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704d003fe83fa56fc5a01331019c043d445770deca81dbbb54efeaa0262d16e4`  
		Last Modified: Thu, 30 Apr 2026 23:50:44 GMT  
		Size: 88.4 MB (88420323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7db3e44f67463d00e6386fd1f1721754750539cf5c9818eb8fe125acc7024a`  
		Last Modified: Thu, 30 Apr 2026 23:51:55 GMT  
		Size: 68.5 MB (68512982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532858b45b330dedd76e5b865b76979d539ad38a918f5bbeb6ef60ec6af8c271`  
		Last Modified: Thu, 30 Apr 2026 23:51:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c93015eb4186b29ff45668b2618da78634214146f9674975370555f2f1f974`  
		Last Modified: Thu, 30 Apr 2026 23:51:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c56aacbef983d1bf01143adf033f2e47576a51b273e4c70036b65bc5142c2d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5077290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cb06bc26a2459df4370b87b3a7aab82fdc5548df401f94b8cd483a98f08a71`

```dockerfile
```

-	Layers:
	-	`sha256:935c830615fbc3f958c0a4a9162f0356f1c20a5d02f4dea0cf36547e82820fd3`  
		Last Modified: Thu, 30 Apr 2026 23:51:54 GMT  
		Size: 5.1 MB (5060767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20dd7611395ccbcb37e546ad503513a53e5ed26a665755f4fd1a95bb48b191e6`  
		Last Modified: Thu, 30 Apr 2026 23:51:54 GMT  
		Size: 16.5 KB (16523 bytes)  
		MIME: application/vnd.in-toto+json
