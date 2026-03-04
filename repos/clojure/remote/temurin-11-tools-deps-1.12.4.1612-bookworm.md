## `clojure:temurin-11-tools-deps-1.12.4.1612-bookworm`

```console
$ docker pull clojure@sha256:dcfd2110ff26aa4a05f55be54dab707232b2781f9ac402c5f4422d2994e5b7e8
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

### `clojure:temurin-11-tools-deps-1.12.4.1612-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:906a0832fa124eb9c79a45181670d767c1d48540022cf7d7f0c415aadf15e015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275473228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38fa38711878a73bf97727a3bfd5f6c528fc3cd0c4b3e799b28cf31cadfb047`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:49:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:17 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:17 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755848a7cb478f5e1766a54eda9dec5bf8321e13cd42933f01f1e9e94a484d34`  
		Last Modified: Wed, 04 Mar 2026 17:49:57 GMT  
		Size: 145.8 MB (145806697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f32c2da40b1a34994973dedf35aa60aaffdc463d8a293d37c41faae7b6f7a1d`  
		Last Modified: Wed, 04 Mar 2026 17:49:56 GMT  
		Size: 81.2 MB (81177112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efbf066f49ee3483e0fd8fa5679965f0fc0991e40862bed94d72be680c49f76`  
		Last Modified: Wed, 04 Mar 2026 17:49:52 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1612-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4a46abd310d353dd8b0288aac33d540b1b9fb00c8f92d92033a07158cd91c852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f55e641a72810f4b34181c3e0ebff11b2000dca4a83ead4a7f170b4d19475b`

```dockerfile
```

-	Layers:
	-	`sha256:8669ae000c0a6f2883df6591e79ea9d35b844de3e2afb3048b81d106f75e91fc`  
		Last Modified: Wed, 04 Mar 2026 17:49:53 GMT  
		Size: 7.4 MB (7398443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9510ae1c33c10118a30d454db8db3b90fc9e4257f4b5b1a0a0b7a7c58d67943`  
		Last Modified: Wed, 04 Mar 2026 17:49:52 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1612-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7c60069289c7be090000222d05ca11de781bcb2e19f79084ed3767ff209c1079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272033377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4a2e9286fd265219a8f1aa2b3def64f37bb599f04badc76357dca84bb3e35b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:48:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:53 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:53 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6895c2e1555a1ee7a26b43528fb703e2030b0b80b188e2f9fc975b070d70e5dd`  
		Last Modified: Wed, 04 Mar 2026 17:49:33 GMT  
		Size: 142.5 MB (142501424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6287eae8157a66ca0fa76b63d0f35323c903f270504ee827cea46cff356344`  
		Last Modified: Wed, 04 Mar 2026 17:49:31 GMT  
		Size: 81.2 MB (81158097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d84da9d4b8b5d6f7ace043743ebe886f45ac9d03c3299ca43a13368ad52356`  
		Last Modified: Wed, 04 Mar 2026 17:49:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1612-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:91538dfaa98134c54ae6c2536cec4aa259908bdd50e715b6d64bfcff8ed28f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac493d3075ea7c5a6044ae37830cd0140e7fab67658dbbe2aada7273c6e4c75`

```dockerfile
```

-	Layers:
	-	`sha256:2a8617fe4d028db3deb47aa29869fe2e0723343d351f0d8fea6c83c53f47d3ac`  
		Last Modified: Wed, 04 Mar 2026 17:49:28 GMT  
		Size: 7.4 MB (7404824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de08f22115aa829f2307fe9bb6fe8e56ec2174cce9a5d49709c8f4ac92521279`  
		Last Modified: Wed, 04 Mar 2026 17:49:28 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1612-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:1f5cae327d5f8df24090558ecd5a60b1c59ee491a44793e9c051b2a6b88628a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272335260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb63e66df46a29a666f75c80bb70c589a5a0d37910945687a57c1b24307aeb00`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:51:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:55 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:56 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:52:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:52:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:52:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4213750e241e404eb6fe26a1532cde1a493011092a65a259711b886cee208ec`  
		Last Modified: Wed, 04 Mar 2026 17:53:22 GMT  
		Size: 133.0 MB (132997797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e38746a5355ee58cfee795e577f3a489e6b20872ac8e49b14252079d087482b`  
		Last Modified: Wed, 04 Mar 2026 17:53:21 GMT  
		Size: 87.0 MB (87000020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acefd75ce9d154a46969d0f310a4c731a0a177b6f43ab5480667c8c19850091`  
		Last Modified: Wed, 04 Mar 2026 17:53:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1612-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:17def0ebfc2ed75ccd6805acafc2d4ce9413e1733b26ca1ee8a868f0c14503dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a9270e008e4f1961a41a81860623a152c3a3fce3e1ea629e365e35139ac771`

```dockerfile
```

-	Layers:
	-	`sha256:d296e7a0653a603736c537da0bd0af4b8074965f4214719a12fd3b394e9e27f5`  
		Last Modified: Wed, 04 Mar 2026 17:53:18 GMT  
		Size: 7.4 MB (7403044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de513049ebeba772bb5e811c6c871200654d25700a7fe1c17a4ec1b63da0249b`  
		Last Modified: Wed, 04 Mar 2026 17:53:17 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1612-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:326b546a5b070e0e85ec63e0ca701de2c03fe2decb08d3b05df8c577f3b186b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253698521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd26b6f2df842fc1bac1e8c02ea3f32d1e2d57e6517ca9b826f7f27fe14b638`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:46:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:46:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:46:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:46:59 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:46:59 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:47:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:47:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:47:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724f84e60ce1b9ebadea7f02a516fcb5bf4d066fb6500750b175ff6967582657`  
		Last Modified: Wed, 04 Mar 2026 17:47:45 GMT  
		Size: 126.6 MB (126562047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01702819f7a91803ae6624419df855c75fe828b15e34c2f7a2071176f35f629f`  
		Last Modified: Wed, 04 Mar 2026 17:47:47 GMT  
		Size: 80.0 MB (79987746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2707e6d5b52852ab1436e999503528c13d88d4294550358e921a5847701733ef`  
		Last Modified: Wed, 04 Mar 2026 17:47:45 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1612-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3dd729ea463e3441e0af5992e016910ec4cadf44ae50cfb5340f0e1e0be3247b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe7a29e798bb5b92d9546df5caefe5147cf1c8e577340d619524b0395fb7170`

```dockerfile
```

-	Layers:
	-	`sha256:8b6dbbdce12913a54a5902d28c5e16f5519e152a1bb9b775c364f3230876b6c7`  
		Last Modified: Wed, 04 Mar 2026 17:47:45 GMT  
		Size: 7.4 MB (7389766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c989e3d06d32cc0fa02f8d33140846c4e84af6fc0cd0f6ab51c408ff76d75f17`  
		Last Modified: Wed, 04 Mar 2026 17:47:45 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
