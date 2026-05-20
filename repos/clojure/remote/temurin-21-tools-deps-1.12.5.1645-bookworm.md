## `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm`

```console
$ docker pull clojure@sha256:a2ea92ee08798e2b5b4b50c5e0755e90aed1f2b0abd54c3d4a6de5099d046802
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

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5d102e34ef29c4bf0250162e7c09616059844c6b5d1326336e56d1cc3e6aac1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.9 MB (287876058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368da0b07611e9d5b5f336ad632097ac6b80d0fd901b80488981cae60c36d73c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:59:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:59:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:59:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:59:47 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:59:47 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:00:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:00:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:00:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:00:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:00:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76882ec5404865bf085f7ce8247879cd991a53bf817e88b4f14895197b89791d`  
		Last Modified: Wed, 20 May 2026 00:00:31 GMT  
		Size: 158.2 MB (158166923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1061cb9744fa4d9b6e7b2411df3dbfd84174ce3feacb5b33bf02b8b5007f4971`  
		Last Modified: Wed, 20 May 2026 00:00:30 GMT  
		Size: 81.2 MB (81212660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ecda896ccbf012834a595317850f44c0597bffad99ee24bfcb22d85c520811`  
		Last Modified: Wed, 20 May 2026 00:00:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5167b771ac7b118a3e598f4530cda1bc364f616749a2b815233fef5767a45d`  
		Last Modified: Wed, 20 May 2026 00:00:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6053884870a36359f621f122e329e1abbb89b7f9178897caaf1e83108d25fbdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6dfa1537d3eec63d08a8a12dce73353758803f7fcef795039a5d98d0fee7bdf`

```dockerfile
```

-	Layers:
	-	`sha256:df37de4a12e52171c4c6959408811774add6c478d56bfc44f36f32379ffca13e`  
		Last Modified: Wed, 20 May 2026 00:00:27 GMT  
		Size: 7.4 MB (7381485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:912383e2161e99c27bbec159b35dcf1e207661a1b4da87f5982c99352e4b2c4e`  
		Last Modified: Wed, 20 May 2026 00:00:29 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3a489319144b72a10bd0697e8625c0e9c4659cc1b48922c81d14edf016113259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286055127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841f53de4bb2c5b66e046ffdd56686a29cce91bde64c6e0be68c0875bcfcdbdd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:07:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:07:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:07:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:18 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:07:18 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:07:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:07:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:07:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:07:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:07:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418e97eccb12837d2ffb3703ac863cff4a89c3412efba2b28dbc08539f2464ca`  
		Last Modified: Wed, 20 May 2026 00:07:59 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2148837da2f473eb9e66e4549e7cfd376cb8fe73e4b58f0d6f54a046e098c8bb`  
		Last Modified: Wed, 20 May 2026 00:07:58 GMT  
		Size: 81.2 MB (81213328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587f833b826d5b3a552847b4695f1e2d153fff2f5b611b624aae5393ace5e0fe`  
		Last Modified: Wed, 20 May 2026 00:07:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cc51d500814cd7198c27bc3002b8ff65f07ed51c5d3558f048b5c9e3127927`  
		Last Modified: Wed, 20 May 2026 00:07:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4de1699ef8afb566f007aab2fce9491f792adee70ccb30d66cc8a35b79cbd8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7404030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a0049405785bcaadb01e32103bdefecd24849a5f005eba068e3dfde7a92aad`

```dockerfile
```

-	Layers:
	-	`sha256:60f7941fcc6e1292b00807e5e3135b91da7af0e15b3f5a0763caa584da77a4a5`  
		Last Modified: Wed, 20 May 2026 00:07:55 GMT  
		Size: 7.4 MB (7387272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5164994ec56a936a2a1b1f8aced0a1b2540e6423cddaa1c71228620a58b86bd`  
		Last Modified: Wed, 20 May 2026 00:07:55 GMT  
		Size: 16.8 KB (16758 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d2bf091370e2fd1ec6911e6b4ea679b9b1bf67777e70416af6d546ee0da438c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297714514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2887f350bc821ab6d899fbb294c28c4462b65e92a8b5facdd348c0d840b90d46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:36:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:36:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:36:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:36:33 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:36:33 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:27:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:27:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:27:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:27:08 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:27:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa7fc9485b4fb59cd58fcb71fcd4db3dba936648eb297bdcd72a79d669b2338`  
		Last Modified: Sat, 09 May 2026 02:37:42 GMT  
		Size: 158.3 MB (158343237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34a3dcfec2dfdeec3cc5ad2825e4a2aa93bacc18c75e68e8e04456b26114405`  
		Last Modified: Fri, 15 May 2026 20:27:46 GMT  
		Size: 87.0 MB (87033444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3402343b535b8aa394bae97057d2e04c1b9bac5f4b49b3b47cba2a6be9e95dbd`  
		Last Modified: Fri, 15 May 2026 20:27:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc6a0c58701ef05d491f4fa08dbed84fb6bf57d93e4eb22ff0046609f2342ae`  
		Last Modified: Fri, 15 May 2026 20:27:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:68b001025036b8563c1cb68b35f1d12ab308abf3c288fc79f2ce54361a958a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dab3d5faa76fb05dec3a193bfdf227393df1a45bafbff014213282aa0ff139`

```dockerfile
```

-	Layers:
	-	`sha256:a22320cbbc099379fc2423672d575946286f23c1598c6707a302bbc4b6236f87`  
		Last Modified: Fri, 15 May 2026 20:27:44 GMT  
		Size: 7.4 MB (7386691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19b8036864f734d5cbe7650a3d2e098a1e3a2a87f9d85cafa3ea489cff595681`  
		Last Modified: Fri, 15 May 2026 20:27:43 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:ff01d35e5c8aafb975366ead96bac7965f5cedd296246ff4c80aff8766768758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274562982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4650c4310215d91bd994716932fe56840967071101e1c0a8817c4fb5663701ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:35:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:42 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Thu, 14 May 2026 23:35:42 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:26:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:26:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:26:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:26:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:26:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25cec1d73807144f8a4fcd73c3f56fbd2782d89baf163adc3be7c86ee3ad419`  
		Last Modified: Thu, 14 May 2026 23:36:27 GMT  
		Size: 147.4 MB (147388349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec735c1c2f57f8940935c18a88a9d79a16baa9eb337259458045d418c1d25d7`  
		Last Modified: Fri, 15 May 2026 20:28:09 GMT  
		Size: 80.0 MB (80025564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e16938ba93c25ef947706ea204187270a7bb45b9e9442a3353d494fabe05f2`  
		Last Modified: Fri, 15 May 2026 20:28:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4fdb597d936cea92812fe6c91d17b3e42e89ad7ac3b366b07537ccd68342d1`  
		Last Modified: Fri, 15 May 2026 20:28:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c8daf752152fd2f7f222e2192f0b07732197b66fec4e0711c4c2924d60ff657e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1182a1b779fb7c3a4cadc48300eb53e399fde1b5c3f9b27048c21f371f5c4159`

```dockerfile
```

-	Layers:
	-	`sha256:c90bab72924ad3c7e50983d9eb858c875c43848a8d063ee021f4713ffcbb8f68`  
		Last Modified: Fri, 15 May 2026 20:28:06 GMT  
		Size: 7.4 MB (7372782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6086425699f27a5474a527c0a21a17c4f8fe5a555c4874a4ce9012d39d1d6929`  
		Last Modified: Fri, 15 May 2026 20:28:05 GMT  
		Size: 15.7 KB (15661 bytes)  
		MIME: application/vnd.in-toto+json
