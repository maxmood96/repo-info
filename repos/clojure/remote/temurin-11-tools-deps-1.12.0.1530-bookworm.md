## `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm`

```console
$ docker pull clojure@sha256:47c2b14751c657e23071b76b8ad0d09be3d33a7a7aacc8eb9688428cee5bc9c4
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
$ docker pull clojure@sha256:dd8e1bfd1b9f789b28917f111ebadb53dc76d044025f84a10974e667ceb314bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271556359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9ad3423dd0c123ad27a6089fe26937308dfd35ff0b340c2e9549dfd7b6f6bc`
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
	-	`sha256:18413843b598d57b91652940578e1de3845bfa3719fe19f5bb681e77af3f0c0d`  
		Last Modified: Tue, 08 Apr 2025 11:19:13 GMT  
		Size: 142.4 MB (142385396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2bb54acd22ef20523d817823ee7a3d565b23607f92c67752c2a73ce7d2dfc`  
		Last Modified: Tue, 08 Apr 2025 11:22:47 GMT  
		Size: 80.8 MB (80842851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e26c796e70577dede4ee4e8922e8a884505522ecb74743ec939a67e35e321d`  
		Last Modified: Tue, 08 Apr 2025 11:22:44 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:19f86e07287bbeb10c22f9c6e6d2f221f84a774158447d492ddfa73e01e43bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7213368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915a4c11635fd0d8be828e35d4d3b4f929418e1108787e65df387293eb1e6d10`

```dockerfile
```

-	Layers:
	-	`sha256:4747fff6da5c6a3a0f51402cef5f0eae0580182f8faa36cb8b430478e33330cb`  
		Last Modified: Tue, 08 Apr 2025 11:22:44 GMT  
		Size: 7.2 MB (7198998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6826bcbc33ebf8c42d87d17e617c3a48c67a1eb62fa5860f276f68588fac12bd`  
		Last Modified: Tue, 08 Apr 2025 11:22:44 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
