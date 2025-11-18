## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:a04b9605d9bcfa71b8c2120122f32c28d4f2ddfd201371cfe987b3a82e0e04d8
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

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b263277053601370a4292af0811136d29deeb7f959b935cd9431e4c216b354f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246620891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a921faa21194be6625809a893b903e9c1ec1f3fb1223e90fb130500e43148b91`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:11:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:11:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:11:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:11:09 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:11:09 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:11:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:11:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:11:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:11:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:11:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d5969a2ed82f25770a91b15ede8fd8798afe66ed20862902271e3ee216d3e4`  
		Last Modified: Tue, 18 Nov 2025 06:11:49 GMT  
		Size: 144.8 MB (144847975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42b5e378441f1c7e611cc459917cb579b9e7ddd816d2a741b47f78e88b95e01`  
		Last Modified: Tue, 18 Nov 2025 06:12:02 GMT  
		Size: 72.0 MB (71995389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce54ca4f7a585e4574475d88ff73a27db17a57f991493b96986a36b43b8e86d`  
		Last Modified: Tue, 18 Nov 2025 06:11:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a6b72c36353c9d5c0da02eba82852cc24cfb3ef5ea968260c0484714478f1b`  
		Last Modified: Tue, 18 Nov 2025 06:11:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:db55a513ecf3e3bb1579a01bbb69d3c50e08a67aa9bc8f5152caf7ec00b4d4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3864550a04e46bf7cc05ed1ef3ca55d59aaec98df36523980825dc11652836`

```dockerfile
```

-	Layers:
	-	`sha256:4c670694d54d779937788ad158a010306751659c6b6222b348bb9c48ef736030`  
		Last Modified: Tue, 18 Nov 2025 07:43:07 GMT  
		Size: 5.3 MB (5256199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e80e4764f41a091f63af3ef1b99612d1de1cb85d2a430bf2b5cafb4e5c89bc`  
		Last Modified: Tue, 18 Nov 2025 07:43:08 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2e9004cf3de452b0ec54ddd3e38a7cd8a9722d337255eb5f00444a345c7096f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245628040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226e7d4ff65be0b8c04b541055011c0981471c4bce3ee8e16c99b97c1499ee41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:05:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:05:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:05:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:05:24 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:05:24 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:05:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:05:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:05:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:05:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:05:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967dd387a1ba781240fae3560d34eab254c38e119ff41f5ce7032b966d47ce3d`  
		Last Modified: Tue, 18 Nov 2025 05:06:06 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab2155ab85675e4c9bb67816d5589013a981e1368440e4a48b10554c974eea8`  
		Last Modified: Tue, 18 Nov 2025 05:06:18 GMT  
		Size: 71.8 MB (71808468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145361a0925c8106cb4b40c4a3c2ae16793a5bea58bc49e6d389a29f8e6a0317`  
		Last Modified: Tue, 18 Nov 2025 05:06:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4d02cf0d9ee34e792bbcd505bd1d16e7298373cf850619959909911371604e`  
		Last Modified: Tue, 18 Nov 2025 05:06:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c5ad3a9f1be10ca9bebeb850d50a5b56117661a7fa03825905b5f98304e48950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72571211cc875d6e5a25b7d4750d3921282a02adf853209c9228e7226634671d`

```dockerfile
```

-	Layers:
	-	`sha256:ef519995367563942297670773e3de47f4eada5225befd887f7fc5209748c641`  
		Last Modified: Tue, 18 Nov 2025 07:43:13 GMT  
		Size: 5.3 MB (5261968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d98685ad0b20b4d95555312dc72d46e6aeeccd9448b58e46aae72381a5c462f6`  
		Last Modified: Tue, 18 Nov 2025 07:43:14 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4b65cc9bb25bedfe4b6ce2e2db849e3c65255617163d969542f648d03ffd2a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255521345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4a8ec7d82a226bab77f6606bc1d1bb9e7df841321f723cf49c5102db833304`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 07:06:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:06:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:06:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:06:07 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 07:06:08 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:16:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 07:16:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 07:16:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:16:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:16:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87c0b8920d1145986dc2b1ab28b2f1ed0575573627003c05e2df1cf5f419dcb`  
		Last Modified: Fri, 14 Nov 2025 13:33:40 GMT  
		Size: 144.5 MB (144525213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bc226951be7d7889b49cd87b3c81215201257cee8274458cb1cb9f80e9e0ab`  
		Last Modified: Fri, 14 Nov 2025 07:17:10 GMT  
		Size: 77.4 MB (77396443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358826bc46df4a6e681e7a537239c8e1da685517a7b3ae39ac203e84c0e4953c`  
		Last Modified: Fri, 14 Nov 2025 07:16:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbb4884ef1f8aaf16db20615a91eae6517c1055c7d9d352f37e6e2d189df9b2`  
		Last Modified: Fri, 14 Nov 2025 07:16:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5aa5e8c2f4c3798632cbf4fffe35535e98a262751b84a4d31adedadc03362872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73eeec9983dcbb67fd0cfdd1e7e0c2880a8edf08b48d606f654f45bb3f2ec54b`

```dockerfile
```

-	Layers:
	-	`sha256:1f1adf8e2017daed23bf94e2cef1abb386ca8614c0a2000a7a51c7a999b3db80`  
		Last Modified: Fri, 14 Nov 2025 10:36:47 GMT  
		Size: 5.3 MB (5260540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8939f43141029b59a629ff8c7d0c245a6bd097ad12b23aff62210e042a081fa`  
		Last Modified: Fri, 14 Nov 2025 10:36:47 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:86dc5101df83fa3bf89b931d41f7cec12c33d9f6734c5f0eb1e1fe3f1668d2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243659116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af120ca190ffacae757edf68de328391dce956c08c2c78445f286d1b2a9674dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Sat, 15 Nov 2025 21:06:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 15 Nov 2025 21:06:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 15 Nov 2025 21:06:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 21:06:58 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 15 Nov 2025 21:06:58 GMT
WORKDIR /tmp
# Sat, 15 Nov 2025 21:30:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 15 Nov 2025 21:30:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 15 Nov 2025 21:30:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 15 Nov 2025 21:30:15 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 15 Nov 2025 21:30:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f51565c831843416c90e1d3853acceb5a5e8eed70cd002dda98e47bceb3fa63`  
		Last Modified: Sat, 15 Nov 2025 21:30:14 GMT  
		Size: 141.9 MB (141889552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462ba749175a9e91fd09b6c3af43465b069b3a82416902cc30bf3cb1de8f92eb`  
		Last Modified: Sat, 15 Nov 2025 21:34:18 GMT  
		Size: 73.5 MB (73492735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9edcbe76a56e48f52efa563028c6121b0a9690ac0a7c380f855f956108861e`  
		Last Modified: Sat, 15 Nov 2025 21:34:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8147397a9a863e7a7462d1b4a8293514e9faf5dca4c92bfb904f3bb4f90105`  
		Last Modified: Sat, 15 Nov 2025 21:34:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fc0ed38e47294eee651d9045fc00e4d280448b7de5320b2e6eba85d75ff0bca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9f50b852dafca7659c1278bc4b044b4e43aa3724c445cf76ef19ed87c71ec2`

```dockerfile
```

-	Layers:
	-	`sha256:ff8194c3335256b1432b4011cbe9d8435b53fcb56a2249f663b38b75cd4d065a`  
		Last Modified: Sat, 15 Nov 2025 22:36:14 GMT  
		Size: 5.2 MB (5243744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:039942f1cf28a649618302e33b3723d63cab160adb612ee91d9d94add602fcdf`  
		Last Modified: Sat, 15 Nov 2025 22:36:15 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5a0f2dedda69e6ecde6afd99ff5d2bc3cb54dbe4f40a86b73c7c86d8dafca44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237648196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8149fe8b68a155855ffca18edaae36bd19bb813022553a2d266c378342c81e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:27:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:27:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:27:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:27:33 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:27:34 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:28:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:28:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:28:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:28:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:28:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c147134912bcb5f024fd99ef3a8779bcbb0eaf98fadaaeddd35e58397454d65`  
		Last Modified: Tue, 18 Nov 2025 05:28:36 GMT  
		Size: 134.9 MB (134859047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e89fec891ce4efb45df55fdbdbb1d4aa03a483dc5a1b77b67a2c5ac4eb8e9e`  
		Last Modified: Tue, 18 Nov 2025 05:28:52 GMT  
		Size: 73.0 MB (72953743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d50505350006edfbe2b07fa5746542fcd5a2b347566da306bc67742822e8c25`  
		Last Modified: Tue, 18 Nov 2025 05:28:42 GMT  
		Size: 608.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df3b4bf49b755637651d121d813cd6690786d8b515c02f5977d19445b9b88c`  
		Last Modified: Tue, 18 Nov 2025 05:28:42 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba644c7a8e7e5cddea3bed6eb4d02013d94067df25d0f3601bf476f3ede2db7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0db50dda8dc0063b8d90b72298bebf979c922d038e227904ed0fba64540725e`

```dockerfile
```

-	Layers:
	-	`sha256:4b6ce650e410c211aebe03377846fe86c3c5401151c63e06687d0d8c89ad1165`  
		Last Modified: Tue, 18 Nov 2025 07:43:25 GMT  
		Size: 5.3 MB (5252123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e408cba8881c80c767b3b497cf3552460e80cb68ba9f15d2b3c7bd90c6746f0`  
		Last Modified: Tue, 18 Nov 2025 07:43:26 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
