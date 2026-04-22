## `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:43ffbcb0be76edd8841d01dc47fcc2ddcc73c0e83b5e45c60d29cb5b800e300e
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
$ docker pull clojure@sha256:e2345f5e87dc16672461dd1a851a1e165cf01eb9dd7691fa3a3d688499202304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192391920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf4a7c071cfe6738f8e5a4ad1913f248a6c2b2ad2ee244489381e7c2a6f2c50`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:22:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:10 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:22:10 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:22:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:22:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:24 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682ef8b1234fd45877643df742e80629c740c299024ae9655f2c483bc55a7bf3`  
		Last Modified: Wed, 22 Apr 2026 02:22:44 GMT  
		Size: 94.5 MB (94455690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb84636ded8c52fc173ff81dc72b05fff558a6772023989e707482bff32c416`  
		Last Modified: Wed, 22 Apr 2026 02:22:43 GMT  
		Size: 69.7 MB (69698940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7dea593cb9f1bfa2e78605178da5f94226946cd3535aa482b4f8aef297d336`  
		Last Modified: Wed, 22 Apr 2026 02:22:40 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb941b7785ee5aefb1eb547373ce6cc0f2a8c66d787d4415bdb8d1a3cf8fb71`  
		Last Modified: Wed, 22 Apr 2026 02:22:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:45380942b972e2170866c20159dad5149b6c262b56ec2350840276f07983e556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7881d9bed53a4f501ea5de9263f38612956f4bb1e9d6a46a72a6687b685bfa`

```dockerfile
```

-	Layers:
	-	`sha256:cf3a199241577e1dc07810df23d6171a2a1825be3346f04764f5ac62623553aa`  
		Last Modified: Wed, 22 Apr 2026 02:22:41 GMT  
		Size: 5.1 MB (5081671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6aee3af5b3e5766c3cc84a2d8822f54be7d4414a1c69b815d886225d9ec08e`  
		Last Modified: Wed, 22 Apr 2026 02:22:40 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dbeeaa5d872bdf8fdce5702adf758ceed2e9029417c5a3e826e920899ec329d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191204511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f125ab80204b9531ba18e6dc96ffcafbe5da41ad82bd599981f90f70086e85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:24:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:24:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:24:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:24:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:24:53 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:25:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:25:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:25:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:25:08 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:25:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ae0d6ba6699934d724194d508cc00803f025eb8f0f16394764435c36bc6f98`  
		Last Modified: Wed, 22 Apr 2026 02:25:30 GMT  
		Size: 93.4 MB (93395168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffb141731e9161f649eeddc28e0d7ecafeae4240caf818b8260b411098d845a`  
		Last Modified: Wed, 22 Apr 2026 02:25:29 GMT  
		Size: 69.7 MB (69692187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d37727338879068ecc3dbf325dc5e6dcf9ec81b666e91cc68b634a6e9d8117`  
		Last Modified: Wed, 22 Apr 2026 02:25:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b1c9152ecd7aac8c325ec742ab2746b2b6cd6ef7ebe589dcbe69b159177ff1`  
		Last Modified: Wed, 22 Apr 2026 02:25:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:96f62246add58ec5eba5bef1ef83dbecc37c97f35263aa52300c96ccf7c08fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5103376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f5ee6bb9fb0c2764076aadba7ed094d5d26af38ebb08e1830c99a4fd147eb7`

```dockerfile
```

-	Layers:
	-	`sha256:b1a7a3de93d243549717a0cd6f68e89e52255f845d258b2303799589b67aec08`  
		Last Modified: Wed, 22 Apr 2026 02:25:27 GMT  
		Size: 5.1 MB (5087429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0a1ec50eeceb5f52bce2f1ad34c56038633f3a6cca27c0806d6948f83c790bf`  
		Last Modified: Wed, 22 Apr 2026 02:25:26 GMT  
		Size: 15.9 KB (15947 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:9efe0d42412b888f6be833d4063f360c15c5e36ecb2ef425416a5a9034aaf321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201390478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed3129635f61e1b4a711f1c564488ca874a206c4ee77fd683f5982da9ae015f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Fri, 10 Apr 2026 00:50:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:50:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:50:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:50:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 10 Apr 2026 00:50:35 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:55:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 10 Apr 2026 00:55:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 10 Apr 2026 00:55:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:55:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:55:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecfd0096cf42a4b346149c8884e2883a5327fa6421d13906fd62b73146a1a3f`  
		Last Modified: Fri, 10 Apr 2026 00:51:58 GMT  
		Size: 93.8 MB (93781481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c098c4db184bace32ba06a24bed28be67d7e12b28d66b1ec7fef1de7045421`  
		Last Modified: Fri, 10 Apr 2026 00:56:20 GMT  
		Size: 75.5 MB (75529491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4974969adc809192268022d639ce3fab8e8ca74fd93f457817f1db8450f6a2de`  
		Last Modified: Fri, 10 Apr 2026 00:56:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae64320daa98e7ec815dfcf1dc194ef59db00a8880216877fc06546ab6220f34`  
		Last Modified: Fri, 10 Apr 2026 00:56:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:413b66143b0e9e6341dcec21197b2073593836c153487884adbe46a8d7adb7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9e32a97ff960c422f9fe97c0199e0f79d2dd84dc4217d00fa6ea100eb35f2f`

```dockerfile
```

-	Layers:
	-	`sha256:f0f094cab565321cb2188f1f8c338182e5dc0d600ad06d08fba93aa611732253`  
		Last Modified: Thu, 16 Apr 2026 03:17:20 GMT  
		Size: 5.1 MB (5070765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfbe8be76697f7dbd6026a29218beccbb5d5ff0656f4197a584187de5b7965a`  
		Last Modified: Thu, 16 Apr 2026 03:17:20 GMT  
		Size: 15.9 KB (15877 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c7d28e53b158b39e5b71dcdb7d121609a7a7d34eedafef7ab6c56691be8d4879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (185953310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec3831a42faab043469d83a19c271d102ccea1a47c49be8f089c4a94487d3c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:06:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:06:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:06:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:06:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:06:51 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:08:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:08:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:08:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:08:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:08:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c6ea417d5ab31a608e273e6f14bf4055de86e0cd7929dfbce786005714ea0c`  
		Last Modified: Wed, 22 Apr 2026 04:07:29 GMT  
		Size: 90.5 MB (90547719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f04080237e53f1415c1dcbb54fb7a8d022917314a71b95a62a395f73a8fdafa`  
		Last Modified: Wed, 22 Apr 2026 04:08:38 GMT  
		Size: 68.5 MB (68512988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa70254189a5b617c8084b8322172ab068eb72982884eb748fe7ed65ff128c4`  
		Last Modified: Wed, 22 Apr 2026 04:08:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aeba7e68b750cf4796b9f3ded73efa0994154d9dd3a1e848c76345a6023b28d`  
		Last Modified: Wed, 22 Apr 2026 04:08:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:066b3b08b2e5a1e39d985ce2c238e575d4eb14ddd16d1ee6167270024740ae3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19faf0d7837795b104fa3eea2c6e8eb581d5673fa053e4d037d21828a002608`

```dockerfile
```

-	Layers:
	-	`sha256:efb196741099202fd4b55d4e125cd74331c0a18a778de0770b3c8cb51b8518f9`  
		Last Modified: Wed, 22 Apr 2026 04:08:36 GMT  
		Size: 5.1 MB (5058178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:132e83b9111769e748e7010b41dc5aaf331b5bd10a77c7538989df8db50d3f0e`  
		Last Modified: Wed, 22 Apr 2026 04:08:36 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json
