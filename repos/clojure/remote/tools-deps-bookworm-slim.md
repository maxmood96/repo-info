## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:77ae569aed2c23374bf2a68a603f5c4d644947a034400830c917d53e02a57360
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

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6bb205f18a02997f9d168e1e379d1638421c5b2f37330084bb3831f30988f24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190510849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3768bc7d8fac594fb84d7764cb1ac377a7ee851bb00177e51a453a5c6c3801`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:28:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:28:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:28:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:28:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:28:17 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:28:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:28:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:28:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:28:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:28:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3279ea37d9d9aa70b4084a8124199c3583ce33d807e3933702b46bdb9bd57e7b`  
		Last Modified: Fri, 08 May 2026 00:28:53 GMT  
		Size: 92.6 MB (92574596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372707a287d348bd3e9f9ebd3edd6077c992253ea7ede1dd68ab29f9cfc368c3`  
		Last Modified: Fri, 08 May 2026 00:28:53 GMT  
		Size: 69.7 MB (69698967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b88e304da5aa33139776825287fe4a71147eee7833059334da5c270ef79a3d`  
		Last Modified: Fri, 08 May 2026 00:28:50 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917a5ca7223c188a04ab51c51526ecb3c6e0981265a99dc9218b82109b38e830`  
		Last Modified: Fri, 08 May 2026 00:28:50 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8bed26cdca9e48b9667b16d04726555f2eb777494ffed38f40e63d85e255ac3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5101563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be25640932e4dcb0c49a59fb81a092230b20fcdba6f6af2dce3d4f2ea80d884`

```dockerfile
```

-	Layers:
	-	`sha256:94a2d6389ee48370c58eedb52541428523aa97e1dd333b83f7f6e83bfb70eda1`  
		Last Modified: Fri, 08 May 2026 00:28:50 GMT  
		Size: 5.1 MB (5084884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0593d289ecad0f13696ec3c8ff7422958b8b87e2a42b8d2105ee10e58923d9e2`  
		Last Modified: Fri, 08 May 2026 00:28:50 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:tools-deps-bookworm-slim` - linux; ppc64le

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

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4d455e94b23a85a2b5dad1c217262065c4d30dc71e23e4b567e2bf994858da10
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

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:baa733742aba544c2d5811ada171ca0739ba69bc35f529968dbab84586ebb91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa9908577568d24a4e9ec5d52d8dce024d00103de0445310e980ebe52db4a6e`

```dockerfile
```

-	Layers:
	-	`sha256:ee6d29c9b30effea1d551911dc3371d403b57a04bf969f15e29051ee65383007`  
		Last Modified: Fri, 08 May 2026 00:41:11 GMT  
		Size: 5.1 MB (5060767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c961289296499c3e45d7f5891912db916e1c558f7f56399fd24663e76c9fb438`  
		Last Modified: Fri, 08 May 2026 00:41:11 GMT  
		Size: 15.7 KB (15726 bytes)  
		MIME: application/vnd.in-toto+json
