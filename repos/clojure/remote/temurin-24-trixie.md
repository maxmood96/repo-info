## `clojure:temurin-24-trixie`

```console
$ docker pull clojure@sha256:43fa27558e008e7c19235e4fa95bb0e3308d732f2c44a7187cf57c0bcef544cf
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

### `clojure:temurin-24-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:d36a1f4ae8037e20e05bec3eb3832e534a5388bbd4ff25ac1f75627538700cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.5 MB (224459082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb06bc708537f7f6c25978546e24bf4b30a5a18ca09fe2b78e5c520c6b84808`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef547f9b3dd8806de5c3d1326d7da024992795e3077aabcadce6138a3b1cc81e`  
		Last Modified: Wed, 21 May 2025 23:34:03 GMT  
		Size: 90.0 MB (89952000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35285005d68cd07ba7d693a25e3ba2004b300bf9d3fcc5f232f601db5ba6498`  
		Last Modified: Wed, 21 May 2025 23:34:03 GMT  
		Size: 85.3 MB (85259132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f2eb9d079a68028d4230e3b6be90e39b3296b2bee1bb5bd2310a03702f5367`  
		Last Modified: Wed, 21 May 2025 23:34:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f0e5946334ff37505b2e184de08150164f476cc30685c7548ea3fc74390752`  
		Last Modified: Wed, 21 May 2025 23:34:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ff4975192fa9f5d40ab74b50ab5af7a94c1c6862efa59bb0df51e0ae532a20b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7284852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e6f7cd35b77e1c7625130481b985423855ed04438e8c33981b325d41f3bd3d`

```dockerfile
```

-	Layers:
	-	`sha256:5c3b54e063bf773218cdb51edc97f13e8642838e15ee8e023f6171b26a93f98b`  
		Last Modified: Wed, 21 May 2025 23:34:02 GMT  
		Size: 7.3 MB (7269062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8981e37aa66923afeca90c393bba0254887a383849d1d6a4c17f18691fdd3ad`  
		Last Modified: Wed, 21 May 2025 23:34:01 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c6f9283832c1d61df310cffec350f24396a16a2001d2b859c65d955a03c2231e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223888708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c33f1ad1a9b21769d2871bf35907f5736ae050ce7a0ec6eb0d352435c5874db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Mon, 28 Apr 2025 21:23:23 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd3f46f8509be2e8269dbababafabf79f4ab8c9edb9b2e5e44756fabe24b705`  
		Last Modified: Tue, 13 May 2025 18:08:31 GMT  
		Size: 89.1 MB (89091184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423c8aa892fe9ff225a339615390a338b2061d7647d02f39c6e49756f80f9627`  
		Last Modified: Tue, 13 May 2025 18:10:41 GMT  
		Size: 85.2 MB (85172361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9235a887f968cf63713413b1d005ec7402acab31935306531d5172504b16193c`  
		Last Modified: Tue, 13 May 2025 18:10:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8f23d04e9cefce7666521476d866892cd38837a9bb30f867bd6975481ae525`  
		Last Modified: Tue, 13 May 2025 18:10:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9f149abd302d7c820443711f36987af4a10745fb734940db576f6771100094e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7242750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39319440ce21fbe0e698569477489300418fadaa8e2470d528ea52776857c184`

```dockerfile
```

-	Layers:
	-	`sha256:d5cad05005a40077865a1314d75ae147a5030a8e78f9cb20a8419e2b76e72ad2`  
		Last Modified: Tue, 13 May 2025 18:10:39 GMT  
		Size: 7.2 MB (7226842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b168cbf6f6afdcecd2277de5d15dacbcae1a14020a5422e2d02e378dd0bae6`  
		Last Modified: Tue, 13 May 2025 18:10:38 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:5b09772f0891522601d3baa734770454f648245a46825e3ef105ad681ed41408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233735597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8e928e2f5c30bb6f6d7e8ffa8ba0ceb8a181ee823b5f30567e7d23fd833b44`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Mon, 28 Apr 2025 21:25:28 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674c4a3f65801b611fa6629a1a146324b962fe77e75ddd0e9c3fd83f2ba4a1ef`  
		Last Modified: Tue, 13 May 2025 19:35:26 GMT  
		Size: 89.9 MB (89920243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231a0d0b2f6e1e47fabfe89872bcb0dcff48237c5967fc62ecfa5fe53ab4443b`  
		Last Modified: Tue, 13 May 2025 19:42:56 GMT  
		Size: 90.7 MB (90741760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8e9970cda08dc8136e61bfb90f2777eb09595e186891094447a9ba8766cdc2`  
		Last Modified: Tue, 13 May 2025 19:42:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b91ead90f74a033035f062421c02352d9ae129130575edd5830f6a93c575448`  
		Last Modified: Tue, 13 May 2025 19:42:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:23c332d9b5fa51e6e3c6ede4783f1ab458289b02183bf2223b798a8635200155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa84c7c1438b500f8fe17522cf05cf8395724ccf0fdca54ef589b82e29791e97`

```dockerfile
```

-	Layers:
	-	`sha256:771b6e028b879c57fb05cfcaae23c0cbc65e27f62ac4c4c2cbd68aac324d7767`  
		Last Modified: Tue, 13 May 2025 19:42:54 GMT  
		Size: 7.2 MB (7225366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93fe426c6a4e2d302c2ff2e2c86615dacf19bb6534976099710d0b7ed9803167`  
		Last Modified: Tue, 13 May 2025 19:42:53 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:3b389ce51e14da1f98df0c08da083fa40411b5d5b79a0e424d75ced938386aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219575420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e111178da8c925ce300a4ab6f1ae6ef41b3087a7fcc2a7547b05394e72856ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Wed, 21 May 2025 22:36:51 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a66e0017b5778e4bade9bef89ef92a010b6f5851fad922be6870b59cdc2a453`  
		Last Modified: Thu, 22 May 2025 00:40:53 GMT  
		Size: 87.6 MB (87622251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ad83b972f3e73c0c1927aaf6372ee6384833189cd3e48c09a402b4637bc7e5`  
		Last Modified: Thu, 22 May 2025 00:55:43 GMT  
		Size: 84.2 MB (84220717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b209cc370d26cb5333d5a1a897e14b2b03102ed08172e738a8c79344ac4532aa`  
		Last Modified: Thu, 22 May 2025 00:55:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f984b776eb492224d8a03bba8bd84b1d149cdbff8a44bafd453d827c91f0320e`  
		Last Modified: Thu, 22 May 2025 00:55:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:191bd61830ee26ab9a10780841f5cdd540e24ebb8d6f5f2fa228634d3992806c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7272808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec413e1a96b8b4ce6d689cfe4d201b42009542199654a78cbfe2bf28c7ddb73`

```dockerfile
```

-	Layers:
	-	`sha256:2995afe46dff641d4803d95916536c7ba2422d25015b6f6bf3b6f0eb53ba9e3e`  
		Last Modified: Thu, 22 May 2025 00:55:32 GMT  
		Size: 7.3 MB (7256970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d0805cec474bf5ed4e6e7159bc7d3a1b6ef4fd5e0a9ea1a57009e790253a3d`  
		Last Modified: Thu, 22 May 2025 00:55:30 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a4276601a6b15d753cb3cdc7ea64ff4df636c35c3327edba9aeace3cd43f8ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220880336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7244fa66b498482b905364d1accc0572e00309fe68a8df27a52462d4fe7319`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Wed, 21 May 2025 22:31:46 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f38a21a13def6964dc50483f08faedaade5738b51a584056cc7447506d8a27`  
		Last Modified: Thu, 22 May 2025 04:07:53 GMT  
		Size: 85.2 MB (85216727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5917408d205dbd94f53ea805749e4503d3b45690f0677c746777aaa04baae063`  
		Last Modified: Thu, 22 May 2025 04:11:47 GMT  
		Size: 86.3 MB (86340346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284d1aa4a746b1e55875b796e6e11a09db50ea3a4857efbae1924987ffacbbd7`  
		Last Modified: Thu, 22 May 2025 04:11:45 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47910af6a1d915edf9b7536709600fd9f05b6a1c79ac6e5f74b82d8577436fa`  
		Last Modified: Thu, 22 May 2025 04:11:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e7c774522a4407c4b412b72ff1b7abf153bd9f315c7417adcae0041c6782b006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7283322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a1ca141e89b2ca3caf2ffd8f8bcc1c428ed0e0d7a3bf699044bb63a3187860`

```dockerfile
```

-	Layers:
	-	`sha256:5ea59cb371837732653ec05ca8dda265f45219fd149838f788d277ebdbaa0c71`  
		Last Modified: Thu, 22 May 2025 04:11:45 GMT  
		Size: 7.3 MB (7267532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa42f348f4fd61c12d93b308776689b6ee4d192f279d2c99f6e468b2ee283376`  
		Last Modified: Thu, 22 May 2025 04:11:45 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
