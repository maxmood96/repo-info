## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:e09332d1bd895e7f91187b81bcbdfc3e1785751958f054729b6729aa27d2842c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fef840e4e335c587d4e2d6530bfdb11a82ba3fbca53348a0ff33ec569f9e2968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202249869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491463726fb3b57d98a557e38ab122cf47219a5b5fcb66f1bb37b76ca84752b7`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73e989b01405f78fdfe17e578771dbc0cd347fd3e116994bf531b86e85d0335`  
		Last Modified: Sat, 16 Nov 2024 03:51:36 GMT  
		Size: 103.6 MB (103634008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63a04ef54f61f2142b0bc113246336c034bc475b3428d861493d9856b0fb42a`  
		Last Modified: Sat, 16 Nov 2024 03:51:36 GMT  
		Size: 69.5 MB (69487220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dba477defe19958de0def207ee7c8b3f2a4afb14f36cb1956ff8cd05dd9fc9`  
		Last Modified: Sat, 16 Nov 2024 03:51:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0655ae9012ce34f6081e150891d010d025f85af7f7a2f9568f5063db5de3c022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5057093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d281a7a7f0515464a73c480cbce1d2736927428c050df94a5d40de15d08541d5`

```dockerfile
```

-	Layers:
	-	`sha256:3e220a006bbeae7587e8367b83438898f35e4557f635b836348337ff4f924749`  
		Last Modified: Sat, 16 Nov 2024 03:51:34 GMT  
		Size: 5.0 MB (5042798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba381baa1db959f68fbded9e32ca655d00cdbf1b7aec8ee454d5581a7e0517c9`  
		Last Modified: Sat, 16 Nov 2024 03:51:34 GMT  
		Size: 14.3 KB (14295 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:552453709959ba4b1beac255eb4089c60f9b8609af001a49e7c6dd6103fe727f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201240805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0bfa528b5c478f891ed1d64aefe88c47535fe3ac6582d89bd83fd325eea7861`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81788011a7c72bb7b64e7d7ba06b654cf3c457826b14241b9a03dbd607de9f9`  
		Last Modified: Sat, 16 Nov 2024 05:12:00 GMT  
		Size: 102.7 MB (102747711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b419e87441f8d944faa75e3c807dc0f84eb46581c5ad7e50e52491c0f4cda0`  
		Last Modified: Sat, 16 Nov 2024 05:16:37 GMT  
		Size: 69.3 MB (69335094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352425d366459baad27542ce17f5e141571c8d1dd8e6e99ae837af434ed37785`  
		Last Modified: Sat, 16 Nov 2024 05:16:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4ab5f44f7cf3326dc163809d77178c4187fe20da8624d86500cbaee14b4a85aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5063677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c635619d2cec993461ea4838f5c9eabbd51c050499c9bb5a998cc48aeeb5715c`

```dockerfile
```

-	Layers:
	-	`sha256:5bdec757eb744b88757c0f8db0e271d749e4cb7974a4d245a1d87ad50f732e4e`  
		Last Modified: Sat, 16 Nov 2024 05:16:35 GMT  
		Size: 5.0 MB (5049263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66cc970076e76b4520d3793c1164f47bc31c1be8ae8bc7e8d5e0f21e51c9693c`  
		Last Modified: Sat, 16 Nov 2024 05:16:34 GMT  
		Size: 14.4 KB (14414 bytes)  
		MIME: application/vnd.in-toto+json
