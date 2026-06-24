## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:6873182c4afa18fa7678c2b2ef3ceb7eaff6f96351f103e051b3012755cb1b17
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
$ docker pull clojure@sha256:13ef3504bd060ca3d839256112d2ed76a3d6d51bd1e6c52928445cfcc41e2265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253048423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966e6874ad4cfd2a581f89f41fb8cfe0020e1dc7cc65a598145fd85e4623901b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:19:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:19:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:19:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:19:45 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:19:45 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:20:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:20:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:20:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:20:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:20:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2d1d869c49c3af02fef7c554f0665920d663e783beacb5817a4f0ffcc63503`  
		Last Modified: Wed, 24 Jun 2026 02:20:24 GMT  
		Size: 158.2 MB (158166945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d759213525f3abe5be9737f34189e262e16728451e05419b65582f9660bf67`  
		Last Modified: Wed, 24 Jun 2026 02:20:23 GMT  
		Size: 66.6 MB (66642797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026eb66d9aa35681bcba5fcb7119542676fdb812b3b4d55d1b70c44c92cfe8cf`  
		Last Modified: Wed, 24 Jun 2026 02:20:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9752cc0e20f494836a7c36261291c3f5679704b2c1233cf209228ba214bd4216`  
		Last Modified: Wed, 24 Jun 2026 02:20:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4f83cf7b2fd8f63726637be13988911f6821c8da3cb509724e0aa1be6ca795b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b0eb76e3458acf78233d47d469445e07e1b5c95504022d9fcaa9881b462e41`

```dockerfile
```

-	Layers:
	-	`sha256:679072371ffc5f6c4ba20f83673b5ec80de7d0844b7218ae1bf7513b5ca260ac`  
		Last Modified: Wed, 24 Jun 2026 02:20:20 GMT  
		Size: 5.1 MB (5115851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbca8815b4c5b1cef7310c9d9544afafcd18038696fff38bbc3ffc914b5f5c73`  
		Last Modified: Wed, 24 Jun 2026 02:20:19 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fa17386eb3ea0742a20a345ec50152ffb822ad156334f88754888792d2b3680f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251228079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c2feeed6a05169283c2fa7d6b78833290971f10783c87adce0ae2d935da3e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:25:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:25:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:25:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:25:59 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:25:59 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:26:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:26:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:26:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:26:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:26:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f18aefff1f7a59c8b8b4356d25fee763811f17dc1e1a63105c46349ca6cc016`  
		Last Modified: Wed, 24 Jun 2026 02:26:36 GMT  
		Size: 156.5 MB (156461287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7677f6393d2fcf68745d01df274802f689057a9623d7cfaf47e5cedf72e200e1`  
		Last Modified: Wed, 24 Jun 2026 02:26:35 GMT  
		Size: 66.6 MB (66643333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9478fef3d7f6958533dbceb681c7cef7526996f164a0c48eb855d844bd27bf`  
		Last Modified: Wed, 24 Jun 2026 02:26:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0409a60f51d8bd361d39df4f47110b10a0ed1c317a4afe71454b6e8889c4659`  
		Last Modified: Wed, 24 Jun 2026 02:26:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:31104b84cb9f157446bef4dd1b3bf4bb5e712e13ca75f5e0535233fcb76588ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccb6615ca7b38d20669ed5ae0e51737f00e5c8f8cbb54e5ac3d53766baf61db`

```dockerfile
```

-	Layers:
	-	`sha256:d8f06591df0f27f650d006df265818f8bb7c403685bb7f19a81d1b1254596b4b`  
		Last Modified: Wed, 24 Jun 2026 02:26:32 GMT  
		Size: 5.1 MB (5121612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16cb03a6de9ef3605597f079c2b46a9ab6cc1a370dfab0d42b5b98bdca991653`  
		Last Modified: Wed, 24 Jun 2026 02:26:31 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f3d589adc3b50bdc0d58b9cb86e4ccfb4911c97d13122af437e22ed98474bdde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262902574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19030bc6cf6250cee62cb0758c9fec2810da67c54ae82a2c66aa7d2fcae5ae6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:54:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:54:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:54:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:54:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:54:22 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:51:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:51:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:51:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:51:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:51:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e41ba91bd198088eadb03a3c25545d904cf2490691f50cad346a585a8741f3`  
		Last Modified: Tue, 16 Jun 2026 23:57:21 GMT  
		Size: 158.3 MB (158343240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae475647756fdd153bd9f29c0b8fabad9bae8f5197003de852c2e27e784ce0ab`  
		Last Modified: Fri, 19 Jun 2026 02:51:43 GMT  
		Size: 72.5 MB (72476357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7437237bf82753108a524dc96421224eefb13579517ad60befe7f4d018c188a6`  
		Last Modified: Fri, 19 Jun 2026 02:51:41 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b24fb6e9645776f5efc2d1cc8924ab2688b027e5cb7462b8cb788c684c07a5`  
		Last Modified: Fri, 19 Jun 2026 02:51:41 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:db76ab1b21a5d191c112bd989057ea703dc73a367e66a6b668ed86d86bf019f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a314bc9a603e020025ba65368649a3b676013361d68578d6f3a068ca917c3e`

```dockerfile
```

-	Layers:
	-	`sha256:595fed261c96145907bd11eca1b9e2e6a6eca405db10b20e1dc57fa3d509693e`  
		Last Modified: Fri, 19 Jun 2026 02:51:41 GMT  
		Size: 5.1 MB (5121009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e709df68e31a921de4870276af022d6fcf44aab7259d12cd4d9bd612ab286b`  
		Last Modified: Fri, 19 Jun 2026 02:51:41 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e7ebe4bd6e0065c404dd8e2ba18247fc989088e150506efc490611973e488ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239735033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d15df63bf79db63aa65942fd9ef51911a62653bd8d36f2239224cb99da294b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:36:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:36:47 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:19 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7c23db7ea29bb7aa16742bb5f7f37601f5b9a0301d0417f6608ab147d6a0ad`  
		Last Modified: Tue, 16 Jun 2026 23:38:27 GMT  
		Size: 147.4 MB (147388339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611671cc9fc8d153994aaf3d80afee434541de7f7d4c74d43060c5266022918c`  
		Last Modified: Fri, 19 Jun 2026 02:20:42 GMT  
		Size: 65.5 MB (65452145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3979b6d27880b7f6e518d21212e43e0de1087ddd5766601f99b56c68d17a245`  
		Last Modified: Fri, 19 Jun 2026 02:20:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dacee03a157af71a1a689766cc213a3947c43d53d2883ad6b69cf43b3553868`  
		Last Modified: Fri, 19 Jun 2026 02:20:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a2d35441ef8a8b84196b8db0b5f9cd2f9d3dde9211b9749710e04c2a457ff6e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7886aae06a4f8310a2ca3ed1ba2f21afbedf84d0c64875dff435d5cd9095bb51`

```dockerfile
```

-	Layers:
	-	`sha256:69a740d387a38e7121db15ee1d81c4bf53ca1347fcf2287170c02294b19c4f85`  
		Last Modified: Fri, 19 Jun 2026 02:20:40 GMT  
		Size: 5.1 MB (5107172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96fe41019e8b793f7faa67f36fd0a695e590bba97a1007d7f55b9d85035e2b2c`  
		Last Modified: Fri, 19 Jun 2026 02:20:40 GMT  
		Size: 15.0 KB (15035 bytes)  
		MIME: application/vnd.in-toto+json
