## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:4f9b39b9fed7dfcc68b22b69d5a62779cd31b18529db37970eb2a86ae4b24236
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:79c3e7252e9f6f8528ef0d389082764f666cb79596483d88b40f221482461d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235919435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52c3bd7325200bfc2860addf7005113c16e421fa01cce2c42c418e869d060fb`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4697b9d20f4742c3f5a093f91744f913f0d3adc70a37062e3cc655151bd84b`  
		Last Modified: Sat, 19 Oct 2024 02:55:28 GMT  
		Size: 145.5 MB (145549936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4c514bd57896640cd3edfd9d101759298498971ce727645af18aefb82a1b92`  
		Last Modified: Sat, 19 Oct 2024 02:55:27 GMT  
		Size: 58.9 MB (58940053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc29c217a533582c53cbe96ae596f6a13ca9c9f69d59c8eca4bfc8fc5329a457`  
		Last Modified: Sat, 19 Oct 2024 02:55:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4211d5392794659d8f13e1640dee2fc50a6c61e7c73fbe018872e692610106bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c211eb0b17f8d799df3981c643eba16869ba7df039398e639cd400e595039e`

```dockerfile
```

-	Layers:
	-	`sha256:7b73493f604b5a6bcc5526707ea5cf1d4988dd9c0b8790d6c379bcc068bf538b`  
		Last Modified: Sat, 19 Oct 2024 02:55:26 GMT  
		Size: 5.1 MB (5145487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f59a76702ec923621889449a9d689531ff40d4bb6d77f5f0ab53a6e28cad733`  
		Last Modified: Sat, 19 Oct 2024 02:55:26 GMT  
		Size: 14.1 KB (14144 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8beca9a28775cb5f528cc7ca1c38d20473e483d95d80c2624eb5a2d081311296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231504457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d03c1d0e5f07601e22b4d1f0f0088fff0a05a40950ec094d355eab10f8338`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6dc61836822badfada79fd5a7ebcd7d72c9f6ee4135bb13a6fa04e4f5fbbf5`  
		Last Modified: Sat, 19 Oct 2024 08:55:56 GMT  
		Size: 142.4 MB (142354770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d37cdea463a495d829a5a818ea7047133865a09436e67cd3bf59bb7fc17c8d`  
		Last Modified: Sat, 19 Oct 2024 11:56:59 GMT  
		Size: 59.1 MB (59073287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec96c5c1b88783d0a5114e0262b80db9d499ca7a5fbdb2244bc863922644da4`  
		Last Modified: Sat, 19 Oct 2024 11:56:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b7e2b63c129a78f3987dfd1acec8faa73ba515413473bc40d96eae249883361a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5166099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e926cd6b7d3b8fdc6d8370f036af349b1565c6901b71153f8b85de1bbef66ed`

```dockerfile
```

-	Layers:
	-	`sha256:db9416ad9883a2baab5d6c76174255d7691eec76c5ba7542b0700b4814819a78`  
		Last Modified: Sat, 19 Oct 2024 11:56:57 GMT  
		Size: 5.2 MB (5151843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa2ef7ab97a8528ea0fc982887da028068b66a6ae171ed5b3bb8206314264c0`  
		Last Modified: Sat, 19 Oct 2024 11:56:57 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json
