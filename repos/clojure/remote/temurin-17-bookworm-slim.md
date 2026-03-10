## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:867dc2ea02cd6cf670528bc3295da5217b0c42ea0df596783ebb9e6693e7a84c
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

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:01d1c9e3be4f298239d42e787e2d313237ad0a22d1b2f8e299f3ea1b08de44d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243567973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aea2cb6349eefd057ec43591c2a34afadee7a61d6c38fcb54b38d486da30e54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:34:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:59 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:59 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:12 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4724b266ebdaf1b4d3a279ebab55ac85472887816edc971287ce72e54b370e`  
		Last Modified: Mon, 09 Mar 2026 20:35:32 GMT  
		Size: 145.6 MB (145628732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e31ede521c3e18cf35adc89ad6ef4d3ba1bbdaa43a36c8a784428a920d2cbb9`  
		Last Modified: Mon, 09 Mar 2026 20:35:31 GMT  
		Size: 69.7 MB (69701919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bae8bdf876a38d3e871b62bce93d124e73cbebdf708b1f60fdc6bc0c84fc796`  
		Last Modified: Mon, 09 Mar 2026 20:35:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5709bb822f4e071ccde6656028da54d5b95e312262ef8f1e6f99ac889d9bad`  
		Last Modified: Mon, 09 Mar 2026 20:35:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c6df9f65acf7ae4035c24821a495b2c6cd77608d9df65f104dc3816a3fe5ee7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ce40004d9a0af72ab07c19c4ba3c0c47b152cbb34f0ea66a482259854b7011`

```dockerfile
```

-	Layers:
	-	`sha256:2a38748074e0caaed52eca1842b908e0542a6777496c26caf25f04fd9ed5a13d`  
		Last Modified: Mon, 09 Mar 2026 20:35:29 GMT  
		Size: 5.1 MB (5116167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0631a5f761f957bae0c5d634698df3c630b7786c79bcb44869c91c3edf4d2a06`  
		Last Modified: Mon, 09 Mar 2026 20:35:28 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5a2a6ac61a3b8cfb91ba5cce1ccd1ef1458a04e7fe1ca839fbf353f8478ac951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242242436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec52442190a339658bfdc02999ee049d0bb5d8d1f1938bcf2a9daf78fc9f2686`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:34:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:56 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:35:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:35:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:35:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:35:11 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:35:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e6d974ef5977082d9356b6eeb6d2c721abbb7a0768e4e3b3c871f15a636e61`  
		Last Modified: Mon, 09 Mar 2026 20:35:33 GMT  
		Size: 144.4 MB (144436179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67e885bd29d88e9056de098254eb719528db20acddba51da89889ae50e2c831`  
		Last Modified: Mon, 09 Mar 2026 20:35:32 GMT  
		Size: 69.7 MB (69689133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa75646a7abb8846655a15785208f732db7f257abd6000c7f4dfc144b621709`  
		Last Modified: Mon, 09 Mar 2026 20:35:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b470ba247aaee92a5adde012d1401fb40134b5118886a9d844602b3f57e4ff`  
		Last Modified: Mon, 09 Mar 2026 20:35:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:275d498978b18f96c55c732c598545e1188c68a79b5aee791384a80f6e34a4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c52be756731a13c2581d393749fcb726dd049b8567f9c670bd44063fe362902`

```dockerfile
```

-	Layers:
	-	`sha256:a3351569a8b8f9fe66fb17a650ac0dcbc2f902697713d1de7182317afb40d5ef`  
		Last Modified: Mon, 09 Mar 2026 20:35:29 GMT  
		Size: 5.1 MB (5121928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ef11b7cc07fb9828ddfb24bcde7b83d69604a82713bcc42f910c9835b3eb01e`  
		Last Modified: Mon, 09 Mar 2026 20:35:29 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:30d9983bdc20202ae719fa6dcd06a5f796a479020dede874d8db53981bb482af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253051192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aded77c21e021bd395eec2f06e4d44086f109e7cf9ba4b304ae3c3ab698d1c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:51:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:51:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:51:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:51:19 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:51:19 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:51:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:51:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:52:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:52:00 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:52:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6794dc00bb6fdaf8b962c369d15f7405aaac04411e7ecbf15a73162317f234`  
		Last Modified: Mon, 09 Mar 2026 20:52:43 GMT  
		Size: 145.4 MB (145438252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f3fa96ed675b2ab57a6ecb8140b534cc08c38e180234f852af24cc6d7d2840`  
		Last Modified: Mon, 09 Mar 2026 20:52:42 GMT  
		Size: 75.5 MB (75533565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3444ef8f59d8f20914dabcb494989e1bb0af6fb800e3ee6ce47d96a97352f`  
		Last Modified: Mon, 09 Mar 2026 20:52:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efd6a5511cecdd7de6eea91e65a2c3dd215e09eb46f497968117ab7177c128a`  
		Last Modified: Mon, 09 Mar 2026 20:52:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1241f1163c2ed8294176ce200955b618309047860fdf256bb2c4bc81a4019b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95eb210026311a594b5c842dc833dda5d5d504b5d3e63d4ff52321d5fe58634`

```dockerfile
```

-	Layers:
	-	`sha256:ff995c05a137f472ebc202f19bbc8fb16d0eb40a83c0792dd052f126d7fc5a05`  
		Last Modified: Mon, 09 Mar 2026 20:52:38 GMT  
		Size: 5.1 MB (5121325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbca8c53941da4d1bf1327e172bb9a15af6344b9f3d3205aaafec8f0c18ba83`  
		Last Modified: Mon, 09 Mar 2026 20:52:38 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b5b699b11ef7ae74de1443d6a4972bcb62eb136d0040096e7c9aad524636c6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231033295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdcfd68c0a1081ee128cdf9b0784ae174ae8120f21417d77df5bda8d77f2ccc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:34:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:30 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:34:43 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:34:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f40c4812b116e842a7e8b49a607546c096afccd07515ec218a2c1c1b134c70`  
		Last Modified: Mon, 09 Mar 2026 20:35:31 GMT  
		Size: 135.6 MB (135627122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e082bac5656d89924b39f248a9952dcd65c6fbce5970886773d39b42494eee`  
		Last Modified: Mon, 09 Mar 2026 20:35:24 GMT  
		Size: 68.5 MB (68513605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fcc257504af90e3fec67362890273dcdd07f91b4e1e83a80849f43e2dde75e`  
		Last Modified: Mon, 09 Mar 2026 20:35:08 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8be159411fb84168e8209c3b04cd90654f23993262ab9aa807211150b5a5ed`  
		Last Modified: Mon, 09 Mar 2026 20:35:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b3d4899ac9d7a300c1d2050068186be213168f042e7a0e83fd398240806bb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1459b5022c00262892c6fc15729004d37b553c3fccaabdb9a38b3a91ad304926`

```dockerfile
```

-	Layers:
	-	`sha256:58ce1fe3b8f11a4ff8be4804f70d21988a82811e418ecf9ca5270dac75347443`  
		Last Modified: Mon, 09 Mar 2026 20:35:09 GMT  
		Size: 5.1 MB (5107488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a42668d5126143b31aa145ca4b473b929cfeef87a5bb75dadc9cc3355a41ea34`  
		Last Modified: Mon, 09 Mar 2026 20:35:08 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
