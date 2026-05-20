## `clojure:temurin-21-tools-deps-1.12.5.1645`

```console
$ docker pull clojure@sha256:2e018237519ace0f071af2f978dd13fbab4d73cdc35e29dcc5ce1dd02eab217d
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

### `clojure:temurin-21-tools-deps-1.12.5.1645` - linux; amd64

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

### `clojure:temurin-21-tools-deps-1.12.5.1645` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.5.1645` - linux; arm64 variant v8

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

### `clojure:temurin-21-tools-deps-1.12.5.1645` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.5.1645` - linux; ppc64le

```console
$ docker pull clojure@sha256:e50a6be7a379827d96a7dfa4c6dc383758045e479ac1d0e684357a2e10c26bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297731281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e94dbf4df25821efc68e976a04b12cb21e6d463a87043445e7db840850b208`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 06:00:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:00:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:00:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:00:37 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 06:00:38 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:16:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 06:16:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 06:16:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:16:40 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:16:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e7fbe50b4d52434b8ad854b561dba737b35bc2557a57acfb7c49c4490a4b2a`  
		Last Modified: Wed, 20 May 2026 06:02:05 GMT  
		Size: 158.3 MB (158343223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51ba50f7921ae2c3620ea6df4b14aafc468d405c05e667ce30d78535f75d1f0`  
		Last Modified: Wed, 20 May 2026 06:17:27 GMT  
		Size: 87.0 MB (87046816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05249a10827ce920bec82c99f31ebd79f4526c163be56600cfad1b0b15322713`  
		Last Modified: Wed, 20 May 2026 06:17:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b589274836ff59a4b12b3aa3b000d2a2902593c0b7209089546076866bfdd885`  
		Last Modified: Wed, 20 May 2026 06:17:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645` - unknown; unknown

```console
$ docker pull clojure@sha256:e7779e84317ac23eaf0d246c91c90f57910d2fdaf6b17f26501b61363abe866a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72485808632bd3dd7830039556d6d4b5dab203d47124e0e6a1028562a2074024`

```dockerfile
```

-	Layers:
	-	`sha256:01f3d4c9e2d64c5a8a114aba2a82ac781223e3731f78cd6c2a2d74d0ad4352c8`  
		Last Modified: Wed, 20 May 2026 06:17:25 GMT  
		Size: 7.4 MB (7386713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2862755ef56302db4ff9806679d3feace8185d200c49fe00e96a8575f48bcd25`  
		Last Modified: Wed, 20 May 2026 06:17:24 GMT  
		Size: 16.7 KB (16676 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1645` - linux; s390x

```console
$ docker pull clojure@sha256:da0298b6375c9dd869ea38632496ed4b26de5a86b77e04eeb9bea8b41e29acad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274570648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e36bc472a5580ecbd05dd769a89de7eb032dd17412a19151aeacf09cfd517a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:45:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:45:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:45:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:45:24 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:45:24 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:46:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:46:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:46:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:46:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:46:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73860fe658c65ad4a5f7d2de80e6569e6b7acde5efb74aebd17e9384fee084d9`  
		Last Modified: Wed, 20 May 2026 01:46:05 GMT  
		Size: 147.4 MB (147388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35414d8a26a28b574e05de3ffd9047bf91d2530d4bfb7745eb7b357bb5ed5c0b`  
		Last Modified: Wed, 20 May 2026 01:47:03 GMT  
		Size: 80.0 MB (80025679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918cc52c0d2b658204c5a62fd5c8eb325938f6b60d729dd0737e0ba8b0bea17f`  
		Last Modified: Wed, 20 May 2026 01:47:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12323916152e67d774754fb665379cc93c709e52d891fb82a8009d84b901742`  
		Last Modified: Wed, 20 May 2026 01:47:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645` - unknown; unknown

```console
$ docker pull clojure@sha256:b2e207fa0116e61fc23f55d29fde0c4fcc0f9a60765d87aa105226efd994acaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d8842ef14920ec66205b3db399ef97c9983a470cbd3aec4a429b81231ca94a`

```dockerfile
```

-	Layers:
	-	`sha256:0ca2db79e414b95f3f0cf5b5956e590bbe39c432c0725e062a7b356e7df05a49`  
		Last Modified: Wed, 20 May 2026 01:47:02 GMT  
		Size: 7.4 MB (7372804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d62b2c85ee49d6e4f81f772cc618e91f4ab5a49d91f08c3021f536fd0e3f76`  
		Last Modified: Wed, 20 May 2026 01:47:02 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json
