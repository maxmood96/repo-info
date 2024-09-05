## `clojure:temurin-22-bookworm-slim`

```console
$ docker pull clojure@sha256:e8b112b50e56972727a4da6c642bce7295e87498704f429fba712d1e99166930
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1c11c4796c634df39b4ee32d55468bcc81b8466a1936041bbb7a0210a2f2065e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254636831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae396d45b9b96c60574da7035eb2eaf677c9242909e761cd287a2dd008bd4c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d7a7022d30ff92b41b9ef6b1b3dee044c6ea5b95f894dc5e95654427c8541f`  
		Last Modified: Wed, 04 Sep 2024 23:08:14 GMT  
		Size: 156.5 MB (156481578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6646e8c79fd4304ab12ff8380d97e7b7e1f6a1243d2e164643510d8e33af3f`  
		Last Modified: Wed, 04 Sep 2024 23:08:12 GMT  
		Size: 69.0 MB (69027729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7891cc11e55ae8ad78295f6e0491ee913af1cee5bed9813f6944253d1ee887d`  
		Last Modified: Wed, 04 Sep 2024 23:08:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1585b1edb27b455498fb1d2bda5368ab846650136759cd8419089c398253ba93`  
		Last Modified: Wed, 04 Sep 2024 23:08:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:31c66c3944cc3bad2f96656fe7402abae224e213cf3842eae8528a93750f1005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15da30635b6f8f208da460a56c146ad10403ca03b9ee97c5f4781d926f08902`

```dockerfile
```

-	Layers:
	-	`sha256:924967ebf25227982e6bfe9617c2bfbe61c4fb1bb7ff257bf183e52cb64e2ab7`  
		Last Modified: Wed, 04 Sep 2024 23:08:12 GMT  
		Size: 4.7 MB (4745158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a07811935894e516b304c51e131b74e4e2ddb54aed845e93a24dbcf53968dc`  
		Last Modified: Wed, 04 Sep 2024 23:08:12 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:19f285f7c95ef3e03d8d75f034ac759e7a5a59f4de3896b9e935337ec8bc2f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252434651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb426b54ed9160d456e322b33355c896395bdb7a5178005e549364ff6000c6fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1fb39c7baa693f1d90f06cdeb26f0916fed34db00c7e3c5e300abff9ca8690`  
		Last Modified: Sat, 17 Aug 2024 06:34:13 GMT  
		Size: 154.5 MB (154503738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e0c5bad4f6a5197bd76067ae47de16ff6d88cfd4f9b49e287c3898be4159df`  
		Last Modified: Sat, 17 Aug 2024 06:39:48 GMT  
		Size: 68.8 MB (68773341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1f66a817cda42f89e73084e50a30883f217a0974781a5e7a510aecaf523fe`  
		Last Modified: Sat, 17 Aug 2024 06:39:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025c5ed36db311b4e99890b31d747147558d0d3a4bb5f3c87c5c802fd6c159b6`  
		Last Modified: Sat, 17 Aug 2024 06:39:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f3d44cc28823e891b03374db503cc48281191c9c9eafc930377e6b5c60243739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7625b49d5c0ce6ea7b8edcb2c21d4574a353ca095a35b43e447c49293b830c`

```dockerfile
```

-	Layers:
	-	`sha256:307a4f76572c2e19b3b33b449bd2bd344497fa33027a423685feacc7adcab1da`  
		Last Modified: Sat, 24 Aug 2024 00:11:07 GMT  
		Size: 4.8 MB (4751543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8588d6925201ce03ed1f9f49faae4632c49d39b1021121446d8e0d0b299066b3`  
		Last Modified: Sat, 24 Aug 2024 00:11:07 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
