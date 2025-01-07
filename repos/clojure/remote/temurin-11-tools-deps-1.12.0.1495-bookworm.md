## `clojure:temurin-11-tools-deps-1.12.0.1495-bookworm`

```console
$ docker pull clojure@sha256:89d593334ab50199730bd5733252cf74965efffdd7c941e36761f5201819e805
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1495-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9f0d56db1ac2a6c1a1859c739153cd391c1ae5087388e22fc88f68ac3908a9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274874908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc34253bb74a204f522ae059702d8f942ce5378e30459d4efb414d985c33a909`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b30dc2afa75e27d7de5c1d1e621bd41b0f123cad15ec5900d728f8e59abfa80`  
		Last Modified: Tue, 07 Jan 2025 02:29:26 GMT  
		Size: 145.6 MB (145601480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5389ce2d263635f544eb1dabd07765c69c27359a3eaa62994fca9d650c5078`  
		Last Modified: Tue, 07 Jan 2025 02:29:25 GMT  
		Size: 80.8 MB (80775720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d538472408f5c7977210eaef9655b0047a1443d664d0a566f9a06876d6edf8b7`  
		Last Modified: Tue, 07 Jan 2025 02:29:23 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1495-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0005d1064e60b7184a8b3c0ce6ee27f987058185c03680507401c0d21a7cbbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7192d50d4c88a6f1105e021d3022daa2885fc393d0657838c460f41e6e826150`

```dockerfile
```

-	Layers:
	-	`sha256:e900ecc656369fde57113c39ee0212a6eda834ae3158d60f1d5d05e3333311aa`  
		Last Modified: Tue, 07 Jan 2025 02:29:24 GMT  
		Size: 7.2 MB (7191219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f511e2918f6789535a2ff3517dd5fdf1ba5b1700d52f60bdb3d42509a0d2ee61`  
		Last Modified: Tue, 07 Jan 2025 02:29:23 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json
