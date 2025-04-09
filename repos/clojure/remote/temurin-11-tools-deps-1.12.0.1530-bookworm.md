## `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm`

```console
$ docker pull clojure@sha256:a521e9ffef7cb392c74b50d35d1e722226c0dac053a905e77659dc886d346d29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:09807bdcb0e2f27ac1f0cee8a5a648324bd700708e20c9222e60b4a7acf26657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275083976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049f13976798fbcd65ec438a1ea829a684443aeffc00d6e547ffb3e95f468975`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc98b112a3d4fe7cfc347c9e50f20e9649e5e6b4ab37f86529784ca60619bdb`  
		Last Modified: Wed, 09 Apr 2025 02:18:21 GMT  
		Size: 145.6 MB (145598778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf70471da1d251496df686fd76f509dab68963324fae3ea351ef72a013c29292`  
		Last Modified: Wed, 09 Apr 2025 02:18:20 GMT  
		Size: 81.0 MB (80994014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f188e591fcc50b6f69cf1213079ab82759fb3985a2cc6675b73e9a8195630c`  
		Last Modified: Wed, 09 Apr 2025 02:18:19 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:59700801a583ab11b3a04e34438f70a57d86e345c1b177f08b7830418c24bbc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7206869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c04ce943da97cb67a7d2ff690b69b00e3b449f88ede225d80b1769c9a722c46`

```dockerfile
```

-	Layers:
	-	`sha256:d4fdc691652a262ccd5e7108de427a3851c7daa121103aaefec35a56fc15aefd`  
		Last Modified: Wed, 09 Apr 2025 02:18:19 GMT  
		Size: 7.2 MB (7192617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:287b7bbbb2448f5a5f4e190bc3c549c3a78e02b1b81f792fb56d22e6d2325f7e`  
		Last Modified: Wed, 09 Apr 2025 02:18:19 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:86d2f332e5e48aee76af6d76a2f67dff501c33b46862dc35bd72c656eb8092be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271556275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05da724583496665f10fa7db85aac2050e4aeee0ebc4adc18078cddead50ae0`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d926e90db35cca6126785829dde031c8fcebbfdb21acc2a6b6101133a074bc9`  
		Last Modified: Wed, 09 Apr 2025 17:20:35 GMT  
		Size: 142.4 MB (142385537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9df1ea92ebc052c341ab56c9e212c6bd9159776dda70fcc2a423705a48f05b`  
		Last Modified: Wed, 09 Apr 2025 17:25:10 GMT  
		Size: 80.8 MB (80842624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3a0fa3b55390140a1160c5d705340477ade90e244baded1f56be255f8195de`  
		Last Modified: Wed, 09 Apr 2025 17:25:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f21ef16de8d45a311b531f2109efa217d22d7bfc811f8b7d65e966235f4e3040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7213368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c302e072032c0b3dd15baccd5497930d21e7bfb4d689bb14afcbdc0976fb68e7`

```dockerfile
```

-	Layers:
	-	`sha256:a0753dccfba4a2a1fb9f35ec26d465e6938e247cd96455c07a5463e70357c388`  
		Last Modified: Wed, 09 Apr 2025 17:25:07 GMT  
		Size: 7.2 MB (7198998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e5577021b39b27c265b1cad801155d29c99ffdbe0103b4d85b7e3eeef72c6b7`  
		Last Modified: Wed, 09 Apr 2025 17:25:07 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
