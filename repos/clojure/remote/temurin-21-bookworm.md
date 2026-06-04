## `clojure:temurin-21-bookworm`

```console
$ docker pull clojure@sha256:aeb648185eb090ed80ffcdca692afbc44337e4bf2801f2356b0ec6ee85408d6e
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

### `clojure:temurin-21-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:68a2a645adf29639c04cc758f93ff5e7b4d9356e09e542fda58a7c00e1669f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284788494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1082e74e88eed0c26721f5bb645124195611406f81d9f16a15affb463929753`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:46:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:24 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:24 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:38 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8f7f7b2db7ba1960263647792f25a71c9d52c234ac4c3ee0644cf7a1bcd7de`  
		Last Modified: Thu, 04 Jun 2026 17:47:05 GMT  
		Size: 158.2 MB (158166939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3754091ebf898211acef4a995a0ecb8bee4ad61e3e9c9d39aeb92ec4ede2497`  
		Last Modified: Thu, 04 Jun 2026 17:47:02 GMT  
		Size: 78.1 MB (78125079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5275bb6afc0a70674afb889b6b0358614ac8359f698f262297d47290185eb370`  
		Last Modified: Thu, 04 Jun 2026 17:47:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa78bc1081f5fbb807edd6aba7a454f74afb8d6ae5047f394bd468b445f8b2dc`  
		Last Modified: Thu, 04 Jun 2026 17:46:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:afddaee655a7726af6173a5d734c3945957cbf86a8b3ffe2031750bde976e9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd974f71eead697ebb1dd0178ea4f28fdae178d5be734108e9b3f7287263de14`

```dockerfile
```

-	Layers:
	-	`sha256:6ba652e1c47d9025b81eaa0b5a096e4b4f4601064a5b09bbe3a41b0cd457cf06`  
		Last Modified: Thu, 04 Jun 2026 17:46:59 GMT  
		Size: 7.4 MB (7378652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e28e3620bc26a811a3355e21bf6ec81cc30e769cf098cb058281ff943b97b46d`  
		Last Modified: Thu, 04 Jun 2026 17:46:58 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:105c0212d3bd6b8abf14b37e74a3754f131e3f9f00b69e344190dfccfd2fed69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282967822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7392573e518832b27a7f8f28ddfbaa11a3288f0ee0b967916c8f11e024f97b36`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:33 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:33 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:48 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22122758a5112415adbf1b41ec50572980981fb51cb7f689340d059c7a8bc164`  
		Last Modified: Thu, 04 Jun 2026 17:47:09 GMT  
		Size: 156.5 MB (156461285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fafcb5cbe26028742fba4ca50bc06ab2df73787c62c4ec575fa4ce745756d1`  
		Last Modified: Thu, 04 Jun 2026 17:47:12 GMT  
		Size: 78.1 MB (78126063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c8d24d9c85089a19271bce4eebc81d503c7cdcf927c7e70be55bee9487719a`  
		Last Modified: Thu, 04 Jun 2026 17:47:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8591820d81e335d9ff1ffb0b1990a08acc3ead4977d53d18732617b13cf8439a`  
		Last Modified: Thu, 04 Jun 2026 17:47:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3baa30002705667d9cf3d01873d6efd41d1811b331a4877e36423e2af031d7b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5184f66197f7c6e955b70dd17808a6d47e61fedffdeb4686769c2889be215a93`

```dockerfile
```

-	Layers:
	-	`sha256:c9d7f7a511b80e34aaee4643f090e0284bdf98f39e23e5b60c9610c55e5e2d3e`  
		Last Modified: Thu, 04 Jun 2026 17:47:09 GMT  
		Size: 7.4 MB (7384439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea36fd3c9bbd3a33c0a12f88fabce7da0e1005ee855b7496cd92368deec84a2`  
		Last Modified: Thu, 04 Jun 2026 17:47:08 GMT  
		Size: 16.8 KB (16757 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:9c6d069ead9c72bb24cac12c1e3c63f145b30807c903fb99df8af55dba78b584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294643848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183610b0413fc2e6589feb4186834c9390e486363740ef3a2143427febe338c7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:58:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:58:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:58:23 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:59:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:59:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:59:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:59:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:59:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026b5eac1372c58bf17e99c04c649b61fc2e6adc57b3b9da967a8850df068955`  
		Last Modified: Thu, 04 Jun 2026 17:59:55 GMT  
		Size: 158.3 MB (158343224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1e775bf6f60a826dd3d40135015c31c5d152319fda825066d69168ba30b97b`  
		Last Modified: Thu, 04 Jun 2026 17:59:57 GMT  
		Size: 84.0 MB (83959381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6656ba49bee3ed3b52da83c445ca5a27598396025d3e473739a2bef99afd9dad`  
		Last Modified: Thu, 04 Jun 2026 17:59:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ea18a6c09f4ecd6408aa54a7fbe3cada6a924a69270aeff2de05b90023272b`  
		Last Modified: Thu, 04 Jun 2026 17:59:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2b072a0e16fbfabbe46936ba20155cf07672697962a55a474ff64057655cd64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b50991437326bda95362c8f401e6cbb22b0a0bc7df8f9eb02deba97d93532dc`

```dockerfile
```

-	Layers:
	-	`sha256:0b90f8df7bd2171dc45872062106368c3e0b000177733325cf26fbe5555ea5b4`  
		Last Modified: Thu, 04 Jun 2026 17:59:54 GMT  
		Size: 7.4 MB (7383880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f96d0ec1e8303bcb2f70c26d7d8e1f57ec3cd580c34c08a73be202803b2b40`  
		Last Modified: Thu, 04 Jun 2026 17:59:53 GMT  
		Size: 16.7 KB (16675 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:9e173ad2af890cdad39e6fb60762e330cb4e1ed56a0f607224710cc9c79c08b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271471385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45257b1a6ca1fa896f1eb7e0ff78ace7358c3de72d79fd081ceba5a4b8e8b110`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:43:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:43:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:43:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:43:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:43:48 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:44:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:44:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:44:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:44:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:44:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492ab93319d8688b385af7b6fa3be6bd8a4bb8dede0f312d857b47af97e4ac50`  
		Last Modified: Thu, 04 Jun 2026 17:44:37 GMT  
		Size: 147.4 MB (147388349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474d7e3ec8680bb9d7c855a8f6f9de740482cc7149a734c58342080b09328711`  
		Last Modified: Thu, 04 Jun 2026 17:44:35 GMT  
		Size: 76.9 MB (76926406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27fbb70aaaf0cdb6cdefd644fdfc9c668ca0695de222659d3741a1e89c0f214`  
		Last Modified: Thu, 04 Jun 2026 17:44:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8541d0daa74feeda5e4cd2b177e15f0171c0b279353d24c1782347220176c5`  
		Last Modified: Thu, 04 Jun 2026 17:44:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b5e9d4965720f695e2864aaca96d77ef5911ad74f5ca260b231c162596cad950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a42ac92d85d2517a7e6e38f5708a247ce5b8f4e1179b803ddc58324f026a0e`

```dockerfile
```

-	Layers:
	-	`sha256:ab907e39788b849d19137c2e57b9b4b065d37e9b0c92a03e8ee2811e220f7ae5`  
		Last Modified: Thu, 04 Jun 2026 17:44:33 GMT  
		Size: 7.4 MB (7369971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85d75745891039ac3b7208ff75e464b837e6f81bc4c425fdcd79c3527b87a743`  
		Last Modified: Thu, 04 Jun 2026 17:44:33 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json
