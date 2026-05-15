## `clojure:tools-deps-1.12.5.1638-bookworm-slim`

```console
$ docker pull clojure@sha256:68641362d84651d17216e6ca9d048cf93287964dea8aa8959098672e59fcb6b7
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

### `clojure:tools-deps-1.12.5.1638-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4151dd6e00ca6ce57c1f1581a60e02df0fc89ce73d728749742dcca7aa121f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190542576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54c465eaefac362a28ec72593e645494df2bab4c983f164f815b3e42418820d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:36:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:22 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:22 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bc74b66010968c1af110295dbd65bcf791ba3d5ec3ed715e1ddfffa08a8a38`  
		Last Modified: Thu, 14 May 2026 23:36:57 GMT  
		Size: 92.6 MB (92574588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b071202cd73090d52337993923379ba6d470b7c0e28ebe8f3de7cd1ad3a03742`  
		Last Modified: Thu, 14 May 2026 23:36:57 GMT  
		Size: 69.7 MB (69730663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc26672cee5860d07330c750cb8cc632f11fa43130bfb98b1b701a9ff255c9b9`  
		Last Modified: Thu, 14 May 2026 23:36:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a93e77f972913d767f8b9bb8f285be4985d94d9ef24e3bf2d2be68cace8ca7f`  
		Last Modified: Thu, 14 May 2026 23:36:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1638-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1983269c03b679dbbdaacd2d005ea15057e62c527688b610994c32cb5870911a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5101561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a77ce327ed3768e1110a31b2285cc1f9544c6a2b4aad2a51d7cbfb60c631fb`

```dockerfile
```

-	Layers:
	-	`sha256:4386412ad36f293569ababaefb32fcca9c4eaedf316641e98bd39afe969569b6`  
		Last Modified: Thu, 14 May 2026 23:36:54 GMT  
		Size: 5.1 MB (5084882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f80ebd48728c3f2c310d61f77be37862c174381c28643adce1d64bde40a92574`  
		Last Modified: Thu, 14 May 2026 23:36:53 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1638-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5c0da29e4302b61c0a2b0932091ad9237f9c25124ef19ee64f2554ce98ffc673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189381537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0881650cfd63da4183df0e0791278d8425b3b2e8231dac5b60b0e8aa29eb09d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:36:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:27 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:27 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:42 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839f7da60d75a9bd9b76df96926e7ad78ff597817ea873a1e1d690252023a2e5`  
		Last Modified: Thu, 14 May 2026 23:37:03 GMT  
		Size: 91.5 MB (91542260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fc5cdef6f43773c83f2ff3c6f51f966fab997a0db6296cd2797243d8ac5b8b`  
		Last Modified: Thu, 14 May 2026 23:37:03 GMT  
		Size: 69.7 MB (69722065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e7f6cf1e92c05d77944016935bc37a8b16be0964c7b49cbb97129e5c4c03a7`  
		Last Modified: Thu, 14 May 2026 23:37:00 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7215adfc6cc17cdddb2f5db7c0b16f74ec6ea0c3f49d0316a5f86cf1056cc3a9`  
		Last Modified: Thu, 14 May 2026 23:37:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1638-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58360489e57c2d8fea0b6e1708b1e84f3e38a15f2469626be22dd15cae31e4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5107485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603f92be7378f08462e762544ce6e09e2aa21651a4658bb79e1f1da8c3d5389b`

```dockerfile
```

-	Layers:
	-	`sha256:0fd31d3ad3c8445e39c05748298272852eebf2ab31d449a7f10a8033846ae307`  
		Last Modified: Thu, 14 May 2026 23:37:00 GMT  
		Size: 5.1 MB (5090664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1714ea8c8d952c15778750f4db7ea7e8c34945f85323ba1bd0ff3e5c2a8f3300`  
		Last Modified: Thu, 14 May 2026 23:36:59 GMT  
		Size: 16.8 KB (16821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1638-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d1a0b93bcdca4566e43e5288e0f6367f6e148e29b71ac47ca6ad297b4ca8ec03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 MB (199559335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febb0a8de8724682a19fef600ce99fd60c585e2c795b195fe643ec188e6e1eca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:42:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:42:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:42:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:42:17 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:42:17 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:52:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:52:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:52:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:52:19 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:52:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2d1c7548cf004fea430b1528d91b72c7b0058d926919d1835a7b351081faec`  
		Last Modified: Sat, 09 May 2026 02:43:20 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb095ad72b299515f093d8a99a22e4cf815a812189cc4b198494b80f20759b5`  
		Last Modified: Thu, 14 May 2026 23:52:53 GMT  
		Size: 75.6 MB (75565808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3a8c4b4c5bb8094dcf76797456e8d8789ce1b61818dc7fd5ec2041bdf81c1a`  
		Last Modified: Thu, 14 May 2026 23:52:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5149ff8f5dd3ff18acfb5b22f4b33f1bab26f27adba0c6212f3c63bcc52e0b`  
		Last Modified: Thu, 14 May 2026 23:52:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1638-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9df178301936de3e9cfcd2b2af6285d9b9480c58b7d177c387f62a78d4327c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5089150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e224c269bd0f51ed69526a920b4db35f249cec625f10f6b968d2ad046f28fe`

```dockerfile
```

-	Layers:
	-	`sha256:70c0eaf32823f666e66a1a367f0a84406755674c83636b7c88802b776430959b`  
		Last Modified: Thu, 14 May 2026 23:52:52 GMT  
		Size: 5.1 MB (5073364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66fab12735e0630adda4c2a9958c6c5cdd38e781a61c3d582dac5f6b1cbcc937`  
		Last Modified: Thu, 14 May 2026 23:52:51 GMT  
		Size: 15.8 KB (15786 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1638-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b81152ff7a6f94bc8fd167901d60372d9ebb57a0bed54d4d7935056b16c0ee94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183857168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33647cb26b684a14f46c0c49a10b61cd3b481ffe125345b65538c350509d26de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:37:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:37:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:37:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:37:49 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:37:49 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:38:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:38:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:38:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:38:02 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:38:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ff53ca1f92c2f307e0a9048298a9fcf9270e8898d762120f6bd32811caf21f`  
		Last Modified: Thu, 14 May 2026 23:38:29 GMT  
		Size: 88.4 MB (88420336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8cda68f1c46a54c463f106eb6c7433bd12e82f06465907c6dde4cafb1eef78`  
		Last Modified: Thu, 14 May 2026 23:38:29 GMT  
		Size: 68.5 MB (68544185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb348f5bdd8726b89b41cd5d34bef7a2d1d19b8791e2b2796d152e5777f67dd`  
		Last Modified: Thu, 14 May 2026 23:38:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d30bd97e2a8ad0f73bcd68360f2d8569195380af8e3691771edd70d6f38aa7b`  
		Last Modified: Thu, 14 May 2026 23:38:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1638-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b3d668d26e1445a1765e73258588b425303733c08daf8179a939e61195e3782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5077444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c3fd77188d6cc86e935084dca2013b6361417b3a75820ff734a8d9c8bbb6a2`

```dockerfile
```

-	Layers:
	-	`sha256:713b93a98bbc7a7bab64407df160f1ab7d533040df30cab0fac0dfeca5df18af`  
		Last Modified: Thu, 14 May 2026 23:38:27 GMT  
		Size: 5.1 MB (5060765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daaf135f35d3f81d3b0c48e3862bd04e08676a11d98b5292299e593c84549d8c`  
		Last Modified: Thu, 14 May 2026 23:38:27 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json
