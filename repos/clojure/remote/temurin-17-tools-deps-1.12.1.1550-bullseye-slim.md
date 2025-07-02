## `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim`

```console
$ docker pull clojure@sha256:c7e3e059ce294bf616b2c1b6787f306dc61689391b5a8ca315e7d10cd2858809
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7a171d7756aa3b49a6514bab2f28ad8e77905840e711ea39cf5432a5818f357a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233897793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e541aa0f00b0c5960eb0601085abd683f1c85519bc50f560ecb1d096c0e7e80`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6730b76d5af51ccc3b319bcab87ceb24db7f72f319da6e8bc117cbd017d79b3c`  
		Last Modified: Wed, 02 Jul 2025 09:52:01 GMT  
		Size: 144.6 MB (144635065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0437a6d72a50606903e1825aba4c81f751fa2e4a35f0203a5c6b197b1955b5`  
		Last Modified: Wed, 02 Jul 2025 04:17:17 GMT  
		Size: 59.0 MB (59005641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a782b487c44a5e7fdd8309c8e204c9dd97d716d57e5ed6295a732ff9847bf41`  
		Last Modified: Wed, 02 Jul 2025 04:17:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d364d2372c4f5129e1d22a64049bb99165cbdf9133b4d4a19d8b3e5bd194663b`  
		Last Modified: Wed, 02 Jul 2025 04:17:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ddc287f79ea1940104476542d289076d5d37b1bc1c371122015c9783ec2075b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fac210f7c247a83fd45e30d6f6f268d46454ba25740b24a296705dc9d1eba4a`

```dockerfile
```

-	Layers:
	-	`sha256:c39548e834ff3209a7b2fbddcc42ee0fa92b7b24db73edf8cd7ea27e993ac478`  
		Last Modified: Wed, 02 Jul 2025 06:37:19 GMT  
		Size: 5.3 MB (5308038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4927c3077053e4f5a4ccea63e005cecf35fc1bf6a718f6de38f756e78c4566`  
		Last Modified: Wed, 02 Jul 2025 06:37:20 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8075a3f760432a31b76763e41957015a1091db4694bd43d9ff26d892e7742416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231395490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ee17a9d9a3a46d4f61d5715d8ef24a99b8a4e76c8896af57a872d323e8d526`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fef6ee0b9946051d8d3bfa169999cf4c735d5970589010a1411377faea8c31a`  
		Last Modified: Wed, 02 Jul 2025 11:51:22 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caca6200c4537ce1698c965599e98d69cf4c5027a9b22bef7dc308730523ce47`  
		Last Modified: Wed, 02 Jul 2025 16:34:21 GMT  
		Size: 59.1 MB (59137676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2931af015189b98c7b58ee6791268b98755de6804ccf30252c06ba689901d7f1`  
		Last Modified: Wed, 02 Jul 2025 12:39:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa295b14611dc79c2870204be565eee8e42a7606aebbb71efd739924448968b`  
		Last Modified: Wed, 02 Jul 2025 12:39:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9c432b8f4c7880f0973df6caaeeae5a13ae78458ddd0d02296bbe43e39f58fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738d2ecf2d90f98069c0e0ff1e638dccbf9ffc20c8e61cd800c3a10d959d6f59`

```dockerfile
```

-	Layers:
	-	`sha256:08756fe0484631ff8a076200c4f2ef790af334ad0aaf9920081b879e5aac787e`  
		Last Modified: Wed, 02 Jul 2025 15:37:28 GMT  
		Size: 5.3 MB (5313770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b766e88a8465f00b1644973ad33eec38037292f0b08dcfc73bfcac1b807f34aa`  
		Last Modified: Wed, 02 Jul 2025 15:37:29 GMT  
		Size: 16.0 KB (15995 bytes)  
		MIME: application/vnd.in-toto+json
