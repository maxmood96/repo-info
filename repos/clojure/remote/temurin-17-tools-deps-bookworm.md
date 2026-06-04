## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:947987be0be876ddb16815f87d772fbcca5f7db4b40a0d850c9952e1cbacae68
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:50e14a5e4641c9f58147ae52dfed5bd4b1a9c7280b77081dc2dfe6347ebe39a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272527050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604c0be31a290dfaf9a94ceb84ec04ecd4a33b7c26d7e3e16516d0c3c5a32dc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:45:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:51 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:51 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:06 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf536f639dbbc3aa495012bb87f5de5bd2c5e67711bd6c6c9fe2e182d67396b9`  
		Last Modified: Thu, 04 Jun 2026 17:46:29 GMT  
		Size: 145.9 MB (145905444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8771256fb4e51e42ba4c95c9d881c21d9f307c4da4510d178feb156e2a1088e8`  
		Last Modified: Thu, 04 Jun 2026 17:46:28 GMT  
		Size: 78.1 MB (78125127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed10b0800da0cf027fcc4d3616cfa3dfdb89cd4b1e8f601276f749080b20a2c`  
		Last Modified: Thu, 04 Jun 2026 17:46:25 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfab92e57b84ec66a877e7b5c607dabbf3e473603a7188c662f2e257ed15ea3a`  
		Last Modified: Thu, 04 Jun 2026 17:46:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:91a047d6120e2a469cb302a4178d224afa757046137371b9d81f034736ccea31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a2ebb51c30b372e4863d7186a5f6ea1b28cac15051dcc57ba3c787b418fa1d`

```dockerfile
```

-	Layers:
	-	`sha256:329edba574670c005be3bac86c3d7c0a5a92ca9ce46593df456bf8aee951dd9e`  
		Last Modified: Thu, 04 Jun 2026 17:46:26 GMT  
		Size: 7.4 MB (7376116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f3ea472cd661e0cb520f30aaebd148ad9fd423ccf79b7f62c95fb122c07e7a0`  
		Last Modified: Thu, 04 Jun 2026 17:46:25 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d9b17fc222a295c4b0dc179c7c811565664744bc6f7f69f84608b00267314395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271230516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cada079cfa6932242b3fd78a3e0610c2c7afbd1a365e9cbf54057710d14e30e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:45:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:37 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:37 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:45:51 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:45:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65687cf30483e04ca99b5c7ad827a0b1aa6ff74e50647599f2e7b8e5a70fcd53`  
		Last Modified: Thu, 04 Jun 2026 17:46:15 GMT  
		Size: 144.7 MB (144724335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca7f13978547c20b934b60f2c865ebfbac1971db310ce458eb552af00747e8f`  
		Last Modified: Thu, 04 Jun 2026 17:46:16 GMT  
		Size: 78.1 MB (78125704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e174b6dfb2e51e10bfe00ac7eec9a01e12fc5546be674c8cba49e5765f642a`  
		Last Modified: Thu, 04 Jun 2026 17:46:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761c6072d567d785e3d6b901f09de6062fb091abc3e365703ac8d560e6cd464c`  
		Last Modified: Thu, 04 Jun 2026 17:46:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7b2f071c26e190c9c93c0d45e38bef0a08d143913b6e0b54ec9d5e7e97bb521d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7635daedfec92f4bac547d577e6316359fc38ce6e8392fb10294eb0ac8175d5`

```dockerfile
```

-	Layers:
	-	`sha256:0ce44e909a95975736e3aad0210483afc669b538132ce443f6f4af381faa2a13`  
		Last Modified: Thu, 04 Jun 2026 17:46:12 GMT  
		Size: 7.4 MB (7381879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f0be306fc53bf5156c29cef9c397652cc203db3fcc3804a7812cd146e01127b`  
		Last Modified: Thu, 04 Jun 2026 17:46:12 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:71e2af0770b4499b7e4af25674c1785fd180ffe11df0d267b89842341b299daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282066861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ec557219c40b7161bfcc52c4827fbea0f62f752466cd072b57ff8ff3c9f6de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:52:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:52:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:52:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:52:26 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:52:26 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:53:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:53:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:53:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:53:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:53:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241ae658f40d10025c8402d2e55ef37b1b4ad486c1fbe0193938d93ae7e3bf85`  
		Last Modified: Thu, 04 Jun 2026 17:54:02 GMT  
		Size: 145.8 MB (145766094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f01a21363d1ed5889ff7a261f26ef0cae69c11e8a5b315658d51c00cab2be4`  
		Last Modified: Thu, 04 Jun 2026 17:54:00 GMT  
		Size: 84.0 MB (83959523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94761067be7512186d6733b4aa1883ed0c3d83647fef451360932e13f3acae26`  
		Last Modified: Thu, 04 Jun 2026 17:53:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e020d4a2d7b53541f3e5e42ecac44d1744f6508b3414dc47b1903fd7e25cf0`  
		Last Modified: Thu, 04 Jun 2026 17:53:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2db98c31e9748e5ccd8fad682f526fcdd6efd3a5eb9387fbbac6ade9b80e4c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b921b8a4d6c9331e7bc8efcb07cc953f219a948073b646570d205f1f98c156`

```dockerfile
```

-	Layers:
	-	`sha256:55ba740bbc623e2aca02a6d9ed0fadf5401ef79ce4eff1fa567bad7ca1ad2fd1`  
		Last Modified: Thu, 04 Jun 2026 17:53:57 GMT  
		Size: 7.4 MB (7381332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acf077409cfc8b611e2744f077bf52f820fa96566effc2f77607abaed8e6c3b1`  
		Last Modified: Thu, 04 Jun 2026 17:53:57 GMT  
		Size: 16.0 KB (15979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:fa2936e44ee79f14d8150dee9612218593c412a554e0b265c0a7e84aee7e337d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (259993458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd02c0fe95ca506ea33c4aa681431b6cc2d043cfe32deb1b8a9009f8ca977483`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:41:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:41:32 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:41:33 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:41:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:41:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:41:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:41:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:41:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251f8b0fe7d3d79863a72f7e24216a634be217c6760664bccd6df8fa71c8dd71`  
		Last Modified: Thu, 04 Jun 2026 17:42:24 GMT  
		Size: 135.9 MB (135910407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf615c27fa3fd50505e8ee598f6349f8813155bf263fc885f922004ecfb9fb0`  
		Last Modified: Thu, 04 Jun 2026 17:42:21 GMT  
		Size: 76.9 MB (76926421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeb53056d2dee4f4f07eb05739ea9f63b915201b6f8a4e38fabc2f3d430a11c`  
		Last Modified: Thu, 04 Jun 2026 17:42:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298671fe2b90c9bcde22bbff085a81465d5b50d4be67e8bb0583ec7809fc44a4`  
		Last Modified: Thu, 04 Jun 2026 17:42:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:64d5e64acf2ed64864cdd1788238491227724cf21ca94709468433d154a39891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7383367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f036cfe12ac08b5ecda10baa7de12e747b9c42de11f4aa907877d3366b4bf59`

```dockerfile
```

-	Layers:
	-	`sha256:d1ec09decd944b529e03124a90514d4436e5b6642d55c7c87dce1869c55bb119`  
		Last Modified: Thu, 04 Jun 2026 17:42:16 GMT  
		Size: 7.4 MB (7367435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ab620fa55ac78bad935a2a05eb960223382e7421c125e3fe23cee41773b97c8`  
		Last Modified: Thu, 04 Jun 2026 17:42:15 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
