## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:20d7481da3c4609979742aa28519209f3b1203168040e4a7b5fa3c6d13d714e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:500df3fb3f7a07f7c642480e26e3ab6297a9e7893df1ba57cb2885d9956665cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233620209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6372151b7e3072719cb8a34242a8e579790cf2afe6fed82950799ab3c080148`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d18a57972ce91991fa1628cfb01f20b2a9cf6142e7a07a1aa6e3b85f2366746`  
		Last Modified: Tue, 13 Aug 2024 01:11:17 GMT  
		Size: 103.6 MB (103611898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161b544dd21924e307995e14a73d3ba58b2807b2c6ddd01c5efe2ad14bf3205f`  
		Last Modified: Tue, 13 Aug 2024 01:11:17 GMT  
		Size: 80.5 MB (80453586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc98e66bd31dd79d58964af87250372d759e0463843d5fda25eee80ba409bdc`  
		Last Modified: Tue, 13 Aug 2024 01:11:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:63ec8b42ea53995b09bce838573f1079d1ec1c480a6b501371a8b04b3a9c0d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7039429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e04540ee9657dd1be39e2e72fd87799e639984cd5bf801ee13129dea36e4c2`

```dockerfile
```

-	Layers:
	-	`sha256:47d3080a9b64d8df53867777bb41c7f50f3e1ec2108cd602ead83e24a12556f4`  
		Last Modified: Tue, 13 Aug 2024 01:11:16 GMT  
		Size: 7.0 MB (7025577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:709ed9ea3b8cfc50988b029eccc015c851be7f6d305d2c8ab03d70540de4e1cf`  
		Last Modified: Tue, 13 Aug 2024 01:11:15 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c141435cc273c74ab2a4cec0343f9047412c6568b1d8146fb5b910283b2ba2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232516935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f151d2c07ba64f5644fcad4bb73e6cbb459579d11f40f22cbc428c2e7461f97b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1a56e08878ad85411f0e218bd104699f02c4529a70c0284bb23803e4bf6a92`  
		Last Modified: Thu, 25 Jul 2024 19:07:52 GMT  
		Size: 102.7 MB (102729199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96592a0f547547ee2b534180d81078ebfce868d5236c7f29e9966593f22de2a`  
		Last Modified: Wed, 07 Aug 2024 19:42:50 GMT  
		Size: 80.2 MB (80198650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7a2d88b943c334950e9fde0bfce7661c7986f22295a1e7e2c99bbc128e963d`  
		Last Modified: Wed, 07 Aug 2024 19:42:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:54ebe31d760b076c6baa695d5b7dec6892dabb7c42978e0b6680899aa997a2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7046351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7615621d7ea708cb9d49519f8b61372d76ebfaf798a34a1d83575b362950cb5`

```dockerfile
```

-	Layers:
	-	`sha256:24c50fdf8aeb4dd204a7454e899ec9284bec2314b701186c24d67b0f174ff619`  
		Last Modified: Wed, 07 Aug 2024 19:42:48 GMT  
		Size: 7.0 MB (7031964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5030bd23963cc6ac97396c5db186baf69baacc2d05e6465bca7ba5e1492364bb`  
		Last Modified: Wed, 07 Aug 2024 19:42:47 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json
