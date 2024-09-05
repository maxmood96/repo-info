## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:3b28cbb600f7773fd517d17bf672fb876e57ead2a459319a2711288b45433422
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:948353c1bd3ac731050c70053588a97cbda16727dd364e9f7cb58686c5971752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275573590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e347d60aac5baa797e74d24564c0c038f58778f4acfa3c78d6ad0ac417d91035`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
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
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f8599f5ed5fd65a4b1e10ef5faa6cfd1b66a037bd4781a1f8a54830993d21a`  
		Last Modified: Wed, 04 Sep 2024 23:07:48 GMT  
		Size: 145.6 MB (145550053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aec33bcde127949ff3561fe22ad79fd68cbca4cafc5d95ee33c3f61a651e9eb`  
		Last Modified: Wed, 04 Sep 2024 23:07:47 GMT  
		Size: 80.5 MB (80466190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e384ff85003e77e36a3f1c3c4bbe54e69a020108d1b4af212e0c8f8e0dc37f79`  
		Last Modified: Wed, 04 Sep 2024 23:07:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:07d0f26670d1b3a3724b3a4bf50fcb516edf5a6689bc1f74fd9739f5c9dc94ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7013336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3beebd9d28a54ed987c841b0508d259a34cdae0fe3475479eb53cc52f0bd0909`

```dockerfile
```

-	Layers:
	-	`sha256:50d8c7093a282ac49981563bcdb8517724e96f9231ab2de5e21bc859bbedf4f6`  
		Last Modified: Wed, 04 Sep 2024 23:07:46 GMT  
		Size: 7.0 MB (6999471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b7d6ec07e74d498746f1df43252ad42912bf57072e687061ad144947fe4a974`  
		Last Modified: Wed, 04 Sep 2024 23:07:46 GMT  
		Size: 13.9 KB (13865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2ba3e7543f04e746ac4947b1e7dbe021b7096cfc224a6207f210d0f78bb99ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272152542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46357a0780e86bdd868684ad70ade8179da662240a58bcbdbaa3959234b2559e`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd64e935a6689bf6a325ad78ce80e24fc9f24773dee803ab3444d4b454bd414`  
		Last Modified: Thu, 05 Sep 2024 07:54:54 GMT  
		Size: 142.4 MB (142354820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7666a1f5f1b941aae7481babe24259f645cee87baf8a4eea7aaa3d23ae6f15d4`  
		Last Modified: Thu, 05 Sep 2024 07:58:30 GMT  
		Size: 80.2 MB (80211453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d9301465f8a1e57d4a63e49787a9297ac7b0cadd117b20a401b26373b8c8f7`  
		Last Modified: Thu, 05 Sep 2024 07:58:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:651d45ad8998dd18b5a341e22b3619e060956740abfc0a31a5884b93ab7d1be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7020259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f21a1d35ac7b3f77059187d10389490261b20e0901d68a03b0f5095d881a72`

```dockerfile
```

-	Layers:
	-	`sha256:17c7042e59fd13288d44408647a8dd1db288cb8aa0c648b5487503b27d77813c`  
		Last Modified: Thu, 05 Sep 2024 07:58:28 GMT  
		Size: 7.0 MB (7005858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0598f368609782601a3b4cfbd23983c7dc5c87193f5cda076faa1fff66053b5`  
		Last Modified: Thu, 05 Sep 2024 07:58:28 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json
