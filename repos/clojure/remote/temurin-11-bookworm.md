## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:a390db9700e4b5947a745938c058a0fd30be08410c235a3b36fbe7571587ed70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d799f71c5085f0bef0945b3b8af805b57f9dd6b288e0056f26a09495216d4c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (276033767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7c5cc73ff51eb904910b948ff5186b62ad04e25655b6220c9482e1df989e91`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542d042e8cfa7b05e815605a3223c632e9f6e144f0fbe266a8d52743a05a2a7`  
		Last Modified: Wed, 16 Oct 2024 16:12:58 GMT  
		Size: 145.5 MB (145549876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3377dfc2f950bb590dc44c5bf35cfbb088e47808fa2f279c939481cc73f180`  
		Last Modified: Wed, 16 Oct 2024 16:12:58 GMT  
		Size: 80.9 MB (80928195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c712c8d2e43b1e36082414ea3a0e708164ee23b57fde6cf8440c55b1870939`  
		Last Modified: Wed, 16 Oct 2024 16:12:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a4a17c8d4c4410508a27ccf4cafe06e73ed477cba50ec78d04c04f04707cf092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7190716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6fab5b2ed6f37b7b13b9ec0845d89b318504913eeedac05d98edceeec7b5ab`

```dockerfile
```

-	Layers:
	-	`sha256:f7e99e02ba57cc0dd3734eca7b58210e09af0b4e5322f316f206cac67cb1d3d7`  
		Last Modified: Wed, 16 Oct 2024 16:12:57 GMT  
		Size: 7.2 MB (7176813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b9cbdfbf4a0171135aeb00776369cf61023c083cdef92f839985c8db721b7e`  
		Last Modified: Wed, 16 Oct 2024 16:12:56 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:da54c5358510c3fabc651dd539211adf5c5dfad84e20d83bb0107fc924c1bcb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272732433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fb69c0b9b84cfc761b11a72d98e6500adc238402b246ff25ce197edc0298e7`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
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
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6544cd678c3107caa9685acfb01eaa6aff2bec3afbf6ae86ad78dd582ee57c84`  
		Last Modified: Wed, 16 Oct 2024 02:11:35 GMT  
		Size: 142.4 MB (142356566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a156891187b9614c5bc601ef7989c03dd0522a5b6a3ac7d183fd883aa75da18d`  
		Last Modified: Wed, 16 Oct 2024 02:16:17 GMT  
		Size: 80.8 MB (80790334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d475ee8349ca8c0e9900ea8da0f080ba7db2ab42afbb400b0ae4fac1ddf51a7f`  
		Last Modified: Wed, 16 Oct 2024 02:16:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:47a3e4d84163c1c3ba2c14d2eb3c795878faa85251e91a1c4b4e6fc66a28f52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7197209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54740bd9c8dffccade3e1e346860fbc826724bec10dc774a01133f4d7fbe4d3a`

```dockerfile
```

-	Layers:
	-	`sha256:f2ac36e2dff86d93def00c317779ae602ebb37bd7d8597cb23054237e2b283d6`  
		Last Modified: Wed, 16 Oct 2024 02:16:15 GMT  
		Size: 7.2 MB (7183200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c849e5dfa5de81782a6a61cb284eb79cd054d04a138b8e1e7ef5f3c038cfd53`  
		Last Modified: Wed, 16 Oct 2024 02:16:15 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json
