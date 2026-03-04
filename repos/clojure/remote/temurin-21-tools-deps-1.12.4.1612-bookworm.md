## `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm`

```console
$ docker pull clojure@sha256:cda813159b766242bf861ed7186cc7417f4763657554477c3f8dbdfb158473df
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

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:224d330a5eed2dc9a0e8abb4e2ba2ab8ff8e480deb3095351a3430e93b2388d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287524235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7779bcaef7b38ee4ec1a6ecf84686292dd51c69cf77dfd2faadab88c963ca126`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:50:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:36 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:36 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f943197e97229c3dc737a71170412df684e10336c50dd9a8030c35b5a64ad896`  
		Last Modified: Wed, 04 Mar 2026 17:51:16 GMT  
		Size: 157.9 MB (157857123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af70480fa3d7e2e448bfa0ce17b0f31e421c18439db9358c788f25244107445`  
		Last Modified: Wed, 04 Mar 2026 17:51:15 GMT  
		Size: 81.2 MB (81177292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ca9b654d865f03401996ede613ec567c778e66ba1fffa39f1d046acfd9c45d`  
		Last Modified: Wed, 04 Mar 2026 17:51:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c0345291a62216f8a4a92b9bd4a3238e73d4aa01bc7d2bb920205e4ff688c`  
		Last Modified: Wed, 04 Mar 2026 17:51:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bb74140417065937992d24c126d3af20cef3c94eb261b2543f38e5caafa2a293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b740c072843e11d32bedeb755fb11780d7fa1996220a64bac5397f82cd3b7b`

```dockerfile
```

-	Layers:
	-	`sha256:ae10ca33da02fb8cbff5e936ff822bd4d0fd968c083ef151faa01eefe146ca65`  
		Last Modified: Wed, 04 Mar 2026 17:51:11 GMT  
		Size: 7.4 MB (7380838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7989157a2399da93111f4e5dfd6f6f3a65b541acd82751511103b6c1ee5db32`  
		Last Modified: Wed, 04 Mar 2026 17:51:11 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:23272b620614f3a77da975c380dd34cf07204891a1ede39ce4b1c81280c7008b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285665343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66aced21e1731e487301c637323bf5bf60fcc63aa203b250deee3c9627642cf5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:50:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:23 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:23 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:38 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb10287e7af0e1be482d592f8b5199edfe019fc56ebad10d3f0a1a0738293845`  
		Last Modified: Wed, 04 Mar 2026 17:51:04 GMT  
		Size: 156.1 MB (156133016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d772e8fc6d0cee6bf58549993efacb6ac0d274943c41ad186965b4a9c42c31`  
		Last Modified: Wed, 04 Mar 2026 17:51:02 GMT  
		Size: 81.2 MB (81158076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84aff44cbf73da541fcbf410522603773d5b490c15853e81eb264cc8d3f4e58f`  
		Last Modified: Wed, 04 Mar 2026 17:50:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c05ae4fe5c06b61aaf3dfb8eee7665ea3b12bc07c977cd42f771afbfdd94d3`  
		Last Modified: Wed, 04 Mar 2026 17:50:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a11154cc24294cfbf5ce1c47db04b539eb4a07b61927664c89a9896eb15bcc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ba2ab81e3c4b182c0fb187be82acb5485747e644390075baaf66c1043a2267`

```dockerfile
```

-	Layers:
	-	`sha256:eddff3a3516f400e685344d3e63cab3421aac5b3e5ef399ea6327f3e80bdeeb7`  
		Last Modified: Wed, 04 Mar 2026 17:50:59 GMT  
		Size: 7.4 MB (7386625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5014cdfc84cb0c24d5212933ddf563edfbaadc717831daf0c68bde849056877d`  
		Last Modified: Wed, 04 Mar 2026 17:50:58 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:aef1df0f5f73809115955726592a72769f9551824c644bf0e889232e53f7f7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297315355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aec5d445937439b0ba919f7def3ad490900cee26d428fd474ba1091c437f8d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 18:03:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 18:03:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 18:03:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 18:03:19 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 18:03:20 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 18:04:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 18:04:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 18:04:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 18:04:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 18:04:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b2f86062ce2ece30a39cca84be6bee97c4ef36f623592a4e3d6b23cbc744d`  
		Last Modified: Wed, 04 Mar 2026 18:04:53 GMT  
		Size: 158.0 MB (157977551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bee31c9729dd35043cef4c2b2c16ab6d89f3db639c1d6ebc512f086925c3c1`  
		Last Modified: Wed, 04 Mar 2026 18:04:56 GMT  
		Size: 87.0 MB (86999962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d60d7382cfd8b3618ce028b9031e8909b5baf1f7ff3a4043431ce72ab1262`  
		Last Modified: Wed, 04 Mar 2026 18:04:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbce773bb42c2ad47a188a300362472677010f2a0189101ea33c63e9bf4acd6`  
		Last Modified: Wed, 04 Mar 2026 18:04:52 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f3efd841aec5799a9410893021b14f7c12d0c75316c1953cebd1de4bc0777624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bbbec152e7204cdb081bbd6edb0054f22aa4d5b30be971165a1db419f85bfe`

```dockerfile
```

-	Layers:
	-	`sha256:1370551fa8397839c6e946432c5615f297f43650612ce8d125c420b744836689`  
		Last Modified: Wed, 04 Mar 2026 18:04:53 GMT  
		Size: 7.4 MB (7386066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fac7a03a5572908cfa7eaaa990adfba45bab7ffbaf3a5e8209e8bef465eb841`  
		Last Modified: Wed, 04 Mar 2026 18:04:52 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:8231e731a160a4871e0c0d38d8ae70926daff855bc274238eb83b69382bb2600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274242381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3537847f70c3a6d6b2385ce28e850ddb5aac4ac6cea28adccd313e8c54d7ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:50:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:14 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:14 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8a7f2fafb1dfa34f107d9c7926dc39dedbfbd8d05e0a59ec6e1e4dec5f9140`  
		Last Modified: Wed, 04 Mar 2026 17:51:00 GMT  
		Size: 147.1 MB (147105249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed07137f0e5db48062f1bd32303b77b57b10759d707ea13ff1d7c2bd0c37a652`  
		Last Modified: Wed, 04 Mar 2026 17:50:58 GMT  
		Size: 80.0 MB (79988003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3942ec26ba07e5d1c7a1a9ef34376957db2b0ee9ffd9cb292dec5c47a8c14972`  
		Last Modified: Wed, 04 Mar 2026 17:50:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf025e0a61da9086932de5d9e7319e9a9bdf5302436d03832335c0efd7f7af4`  
		Last Modified: Wed, 04 Mar 2026 17:50:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1612-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4752ec9d578af7d364eaaf78786f93c410ea0556f225b03730e648e885c4487d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204c7f25d5271f86a57f072c4e711f21eecd4a2b203f4ea46aade6a8466f806b`

```dockerfile
```

-	Layers:
	-	`sha256:7cc59fe905f873dacbd4c681ccf78ea7b7b50375fae2d5b1fe3c62854828d9fa`  
		Last Modified: Wed, 04 Mar 2026 17:50:57 GMT  
		Size: 7.4 MB (7372157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2848366b9f601678f2ff8a89d029bfb84477245efed17a21b550a57a5def7f25`  
		Last Modified: Wed, 04 Mar 2026 17:50:56 GMT  
		Size: 16.5 KB (16461 bytes)  
		MIME: application/vnd.in-toto+json
