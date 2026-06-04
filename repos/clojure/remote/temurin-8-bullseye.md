## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:9f106ed831767e092a7672a14d2c5f1250c1e72476cd5e5b05e33e19ad14d5e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8166e586a6541046502e077fa62f8a75c896e1a7efba176881c102ceab4f9162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175480483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb9acd0cd364cef3aeab9e5ec865983f139f930315b86fd1d99989022edfe3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:41:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:41:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:41:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:41:05 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:41:05 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:41:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:41:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:41:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935f877b84cefbc3ade82e13966cbd717c2750fc0c42aea45d7a3ba2f33255d3`  
		Last Modified: Thu, 04 Jun 2026 17:41:37 GMT  
		Size: 55.2 MB (55198726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0997edbe2f28e311a83000fab707fad0218dceb30d8212382a54b5ccadb71ceb`  
		Last Modified: Thu, 04 Jun 2026 17:41:37 GMT  
		Size: 66.5 MB (66512258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e8a6601add6313a516d96ea6fd79bfc55cc52a522d6124c23cb8eb73da9aa9`  
		Last Modified: Thu, 04 Jun 2026 17:41:34 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bd3453216dae52e7af8a6d7905736a5c8dec284b2b4c989ca91a5fc5e1aca9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7540153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926d075aead0830de215e54a126b83e20f857aff1d7fe2867be44aef8b913f47`

```dockerfile
```

-	Layers:
	-	`sha256:f91a59703ba30fe3946200050747389a1fb7d976e0a13164feccb7930faea2ad`  
		Last Modified: Thu, 04 Jun 2026 17:41:35 GMT  
		Size: 7.5 MB (7525805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e60c321b94b04729f4c9779dae53c8c23741d99b3642cd4b0fb8b216202cc23`  
		Last Modified: Thu, 04 Jun 2026 17:41:34 GMT  
		Size: 14.3 KB (14348 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8dcb7582b0bd89066914c97fbf7a23bdc912af7ce1fcb8adf95ddf57914a4221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173207870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8068740fe71964a61eea12ce813228cbee84a1e8440919b3e9609edf66611a8b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:40:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:40:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:40:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:40:57 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:40:57 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:41:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:41:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:41:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9537acc966cfc058ef45296fe874538f199ead380b7cd621cfbf452fb0fddbe1`  
		Last Modified: Thu, 04 Jun 2026 17:41:29 GMT  
		Size: 54.3 MB (54272924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66af0ed59bf0dca94faf6e2f5b507c887e778f2185c25ceb10e1849bac3b145f`  
		Last Modified: Thu, 04 Jun 2026 17:41:29 GMT  
		Size: 66.7 MB (66677722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030ad44d441495f8d60d1fe214c80edb916f8e1a6fefe917ef6f1edcfd887848`  
		Last Modified: Thu, 04 Jun 2026 17:41:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:825c77aff1cb7ebda6807e4fc0f96a22cdc4635f9dc26067323755de79a0b9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7546070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5916ef1b37fa0683e3dbbf1873a51c263aeabd46b18dd6441a9ffc341014604`

```dockerfile
```

-	Layers:
	-	`sha256:2a8def73b698d9bda086e7dc99d264a8ccbbc651de843210782ccba94bfe66d9`  
		Last Modified: Thu, 04 Jun 2026 17:41:27 GMT  
		Size: 7.5 MB (7531604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ddb680d13e16f127f7e613e7a42c1ca3ad9023448e5a1c5dc514f39a83a4864`  
		Last Modified: Thu, 04 Jun 2026 17:41:27 GMT  
		Size: 14.5 KB (14466 bytes)  
		MIME: application/vnd.in-toto+json
