## `clojure:tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:846ad47217ebab1de70f410406101e62e3010eba59c47e7ee55ebf81a63ef977
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

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

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

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

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

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b1bdc1850e0ef161d916338d9d2168f53ba2fba7fe86164210438c20e43928f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189351997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d410fcdb4f01d29ea49d1be2f971f8520a673912ed827d88478622e7ce0be1a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:27:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:27:48 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:28:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:28:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:28:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:28:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:28:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3687d32ec2aa10137c7512be96bd0fc1bcd43707ed364d12000411d2761046`  
		Last Modified: Fri, 08 May 2026 00:28:24 GMT  
		Size: 91.5 MB (91542285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d27cba81fc6da2b4872930ba50c7ab64bc4ffb1e110d4e063d04611660da460`  
		Last Modified: Fri, 08 May 2026 00:28:24 GMT  
		Size: 69.7 MB (69692557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f920edbc528688edfb268431e35e5ea689ea8f5edecb64dd7d8159e4b97e134e`  
		Last Modified: Fri, 08 May 2026 00:28:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f40cde2985968146fa4795ad4d5a6167fd746bf3a0544d2296d54e923e109`  
		Last Modified: Fri, 08 May 2026 00:28:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7096b139d7a9f7574c6a2d94d36fb60ae81fa0800be383cdd9dae8e0ee2385c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5107486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521fb2d33ef0952d4981c64899588e522c87f093819d245e3cf2847f8cb3a496`

```dockerfile
```

-	Layers:
	-	`sha256:127a16cc644bbfe076374e7031619a26562b3c79e888d41dfc38ef2320fdbcf3`  
		Last Modified: Fri, 08 May 2026 00:28:21 GMT  
		Size: 5.1 MB (5090666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7f40943e81135316857d346287ecf29d002128f9f217f04bdbdcaf6ccd1764c`  
		Last Modified: Fri, 08 May 2026 00:28:21 GMT  
		Size: 16.8 KB (16820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1655a0ca5700d8640b9b01d429e2d22c9b97ebf4d67a9f363eeab33890c15518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199523023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03700fc2fe936b1d9a1b5c6612e4d83473ce479e8f118ff945aa6f741e914fef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:43:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:43:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:43:56 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:47:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:47:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:47:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:47:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:47:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de1619367effbb8009b986da2ea9fbc4fb9ea6adb3d628cb1ec99649f247618`  
		Last Modified: Fri, 08 May 2026 01:45:16 GMT  
		Size: 91.9 MB (91914008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b5037534acb8777b09766551c6cbd39fb6328aae92ebf265485fe20f3b450c`  
		Last Modified: Fri, 08 May 2026 01:47:54 GMT  
		Size: 75.5 MB (75529577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fcda60bf46d033eab9fc328233a32c3c1fe2d67ce1a7b4208cb85b04462ac7`  
		Last Modified: Fri, 08 May 2026 01:47:52 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ece27773f94ea5f988d5e1d2427a2fe821f2a5be4a59552114c15cb7e93f84`  
		Last Modified: Fri, 08 May 2026 01:47:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:acf5935cef5128f53dd4f95187c13c7de6789a81546a4dada69deb1277d1b4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5090104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32290085162ab3feee23f8be6432b33e25dc706c89c70021db0dd9760ae3da03`

```dockerfile
```

-	Layers:
	-	`sha256:b8bf4c229e4a95bcbe5560d0f40f321c564a2afdb78eaad458bb17574bf74bc7`  
		Last Modified: Fri, 08 May 2026 01:47:52 GMT  
		Size: 5.1 MB (5073366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ed4a0649f26725bb2fd3e3cfce891c32a81e38064399f93d559015de4c36e4`  
		Last Modified: Fri, 08 May 2026 01:47:52 GMT  
		Size: 16.7 KB (16738 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - linux; s390x

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

### `clojure:tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

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
