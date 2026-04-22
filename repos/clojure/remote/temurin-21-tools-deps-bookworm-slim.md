## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:e2ba0602b2bf9022b20957f42914abd5485d67db010943bda5261ae00cd5d48b
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a298c035c6fb5bb9f1b5515c17deeb54439b82711053774fc53866c798ecdfb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255793540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4534c9f46fcc7588e26f184e7342ba630a8d3247c27ffcb53928334b16cdb77c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:05:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:05:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:05:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:05:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:05:40 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:05:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:05:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1374c734028c648fe6f3031ef4de1c45fa331fbc1812bc39fdde14ba1bfd433`  
		Last Modified: Wed, 15 Apr 2026 22:06:19 GMT  
		Size: 157.9 MB (157857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8ba986d574e7adb8241a6ecb82962af5a38c19744739071ba0b191f7ef0b58`  
		Last Modified: Wed, 15 Apr 2026 22:06:17 GMT  
		Size: 69.7 MB (69699081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1e0c04ce8bc99eb0c9f8f56aca87ab9fcac9b0b4e54499497ced92bf76d8f`  
		Last Modified: Wed, 15 Apr 2026 22:06:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a243cc90f6d2a2e0958dadd0073f0b0d40ea1a2cd02824b526d74520e4bc5b`  
		Last Modified: Wed, 15 Apr 2026 22:06:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:12548697b9bf74c4e217e44e1e863c82c54065ebc75039a02b4ee6061ebf54fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b60b6668b832c3d617d8426ef8099d919b3c6e7be7a8f42c5e3b60c341e15c5`

```dockerfile
```

-	Layers:
	-	`sha256:10ab5020e9c0c1b44c6998b8a57e458af7847b2e6ce9545a9906abdbd8e12cc8`  
		Last Modified: Wed, 15 Apr 2026 22:06:14 GMT  
		Size: 5.1 MB (5118019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:820201f13460df0a189d3a7ff1bb684cd4d5e132c46548b9c4c07848dbecbb2f`  
		Last Modified: Wed, 15 Apr 2026 22:06:13 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4d70f9e7cd1bf4827df6d2075534f8364151ad4767c7c2ccfc0a10925f40e4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253942718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938a2c845466e2cc03e4deee6109a41e7b0eb25af6a4b62b9fd26c78b8a397b2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:22:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:42 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:22:42 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:22:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:22:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8759edc74fa1b779e499901f463d84f0c84b2349979ccbc3b9fd47ab70a9523`  
		Last Modified: Wed, 22 Apr 2026 02:23:22 GMT  
		Size: 156.1 MB (156133067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b9e0cc0f11edc1711863f0d3c528a76d845780f80c6f08d471c793480a7a37`  
		Last Modified: Wed, 22 Apr 2026 02:23:20 GMT  
		Size: 69.7 MB (69692498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f75ebf496d2565bc9b8f33232d4cad2c958aeee513f50268cf16d7d2a4f81e`  
		Last Modified: Wed, 22 Apr 2026 02:23:15 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfe01c5808b6e755b92e72c39de6859be047266bdb4cc92416888d22292ce0b`  
		Last Modified: Wed, 22 Apr 2026 02:23:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:93212b00e811f13d20af4dfefe27e4e258cab4c00af1f0aa86fca2162571c528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ea7fbb1babea961177a51c2188cb18e32767a8e05eff5712decd5fd5aa7925`

```dockerfile
```

-	Layers:
	-	`sha256:116238aded8b0b4583fa00d13f67a9cef8b0b2bb2584b4a52cdfdf570de37db0`  
		Last Modified: Wed, 22 Apr 2026 02:23:16 GMT  
		Size: 5.1 MB (5123780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a58454346f1893b8e228f0fb86775761368be37ff528b2d413450c002b77ad8`  
		Last Modified: Wed, 22 Apr 2026 02:23:15 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d9d4add37a86cadc64f6ca18f615b020020c1d07ada9c7660fea9c60a4d47245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265586946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83b73a6eec97a7ff274c6058f9ab1bc515d79c8dc2324f64ff11632cfdebc1c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:58:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:58:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:58:34 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:04:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 03:04:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 03:04:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:04:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:04:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e203b9caf09504a0524431e8715aa89e01133d5345e0098d271b086ec7c0ab87`  
		Last Modified: Thu, 16 Apr 2026 02:59:55 GMT  
		Size: 158.0 MB (157977487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3146cb999b00bc60e8fb3093d9e17395e46e7cc910d15380622c7c827b8aff`  
		Last Modified: Thu, 16 Apr 2026 03:05:07 GMT  
		Size: 75.5 MB (75529952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b81ad85740b10f8ab8bd819a208d7d2e499abf0803ce9313c0654afcd08ece`  
		Last Modified: Thu, 16 Apr 2026 03:05:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c4482b634ceb998e5383955076f3d7481eb902d240dcb2d39a7eff50b3c2ad`  
		Last Modified: Thu, 16 Apr 2026 03:05:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:11f11127956dd5a44ca17ad34a22e32f75725ff32632c4d7d6aec0e1c1ce6426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcdeb427c096538863ca3a6d04a44e602457d7dd5e8a7ba37083624d9e33b56`

```dockerfile
```

-	Layers:
	-	`sha256:ce6a58012026fa14a3b01fe115a5c464b332122d9034d159a791167414592f0a`  
		Last Modified: Thu, 16 Apr 2026 03:05:05 GMT  
		Size: 5.1 MB (5123177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2abf0144cc1f5351d6b9421bc3000ca508ccf8b846cc8f8b6882211c29b2f491`  
		Last Modified: Thu, 16 Apr 2026 03:05:05 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b5480d716a1079fdbb47a4b806593689d2d709f8ed5a234920713d834a06c7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242510932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f2b105b57d96c7b29b07db8f6f68d1c66519f2c0ea52e29a5d57b4ccc4398b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:41:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:41:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:41:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:41:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:41:57 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:42:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:42:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:42:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:42:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:42:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a11d38e0f7fad98da09dfa4bfaecdfa77082038533ab04d75a1c54e1f91ad16`  
		Last Modified: Thu, 16 Apr 2026 00:42:43 GMT  
		Size: 147.1 MB (147105251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c215a1b2de8c1dd2f80be2683e0666df3107c689edd8afefe8c227e33d2b26e`  
		Last Modified: Thu, 16 Apr 2026 00:42:40 GMT  
		Size: 68.5 MB (68513005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b877a57c53cfeab2bd4808c55debce61e284d439a12c51012b38db3cdac0e11c`  
		Last Modified: Thu, 16 Apr 2026 00:42:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e1043e91b8a4a946e4ef3f58143257a580d53970ef6eccf1235c4000fe3082`  
		Last Modified: Thu, 16 Apr 2026 00:42:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6d131a463e04bc7756bad5d8f98ea1fcb9de4f87bdafba82892c0ebe19edff1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c451ec0c991f21446a105557de4e26adcc61f5b6c01591dd71992012f6c3bb4`

```dockerfile
```

-	Layers:
	-	`sha256:62267fe28c2e8f21494cba1fcba56f66c658eaf1d86a7bfa98e55f7b948402f0`  
		Last Modified: Thu, 16 Apr 2026 00:42:38 GMT  
		Size: 5.1 MB (5109340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1de1b26d63fba8b7426bf68a09037d7196dd3b689ced5cd8e9aa64ff54e2376`  
		Last Modified: Thu, 16 Apr 2026 00:42:39 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
