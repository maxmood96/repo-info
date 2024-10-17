## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:600d88f869a92a6cb05e9d215490de612080b5d1013813ac8553e8aa37d823c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7fd9e4031eafbaa7cbd5f8d3d5352670359ac3c4f53dfd7922f742f67882ad43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235919402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f987cda7d8d36da7290b3ca1faa5324d5030b3bc62368c9a6aa3da36f3067eb0`
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
	-	`sha256:b58c0ed60345efd5ceced6ad3328a65257bd0b6cfdd2121ecd54a2432036317b`  
		Last Modified: Thu, 17 Oct 2024 01:13:29 GMT  
		Size: 145.5 MB (145549908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b924d75fa5dc663d0beced053fc4c22e13d6865002c61487a4bc439ab70a900`  
		Last Modified: Thu, 17 Oct 2024 01:13:27 GMT  
		Size: 58.9 MB (58940052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb130e22ea74b077ae25bc5e32698133562175e83299cc9f4ff303acfde54904`  
		Last Modified: Thu, 17 Oct 2024 01:13:27 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:92c79368f8f94cbb4420d0a3196015b01a584f22a5b4291e95c95101b6dcc3cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffec44e758f4551993076cf2d13c97ddf7e79dfac12d30d29f66c3b58391732`

```dockerfile
```

-	Layers:
	-	`sha256:4f4d7bc0603731286b75693f0f6554871c9172979304156b54792cbf2e82fcf9`  
		Last Modified: Thu, 17 Oct 2024 01:13:27 GMT  
		Size: 5.1 MB (5119742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c9413ff265956b467a00fc3f65b539dc7f26568bf7fbf49261d66e5bf388dee`  
		Last Modified: Thu, 17 Oct 2024 01:13:27 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aff7eedc5c3334ce2c138de03ecd7df44c43f5f5391917111f30ea747f981577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231506433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474de96895e434aace31ed241cf4de962604a1ff7143f0546dd7994c923c0d8d`
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
	-	`sha256:552c07f22f7a24a94dcd10f61aa1a932f70c4b4c6f411f7d5e6fc0e25d319dc2`  
		Last Modified: Thu, 17 Oct 2024 08:06:47 GMT  
		Size: 142.4 MB (142356620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5020e75e5570d264494fe7246632178b14b22e6f41c813db09a3bac95aea47`  
		Last Modified: Thu, 17 Oct 2024 08:10:30 GMT  
		Size: 59.1 MB (59073413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdc57f6ce793dbf09e888d013b80c5358da6f92fbe1d0a487d8ee9efc9f28ef`  
		Last Modified: Thu, 17 Oct 2024 08:10:28 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee78a726c352fce334f3533a25fe72480fb9904ceb8f1363df64226e57aecc85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4819b3198e87d1e2261081a50c8d207a91b88e984e3e60ccfce4c3a99e85a3db`

```dockerfile
```

-	Layers:
	-	`sha256:44860e6581be918a985311c6f78a4465990fe58d9b664bc1c6449192243ad13d`  
		Last Modified: Thu, 17 Oct 2024 08:10:29 GMT  
		Size: 5.1 MB (5126098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:110b447c19a125edb3fe00d0902c48fda48123e29643102d1e4e383375ac02bf`  
		Last Modified: Thu, 17 Oct 2024 08:10:28 GMT  
		Size: 14.1 KB (14082 bytes)  
		MIME: application/vnd.in-toto+json
