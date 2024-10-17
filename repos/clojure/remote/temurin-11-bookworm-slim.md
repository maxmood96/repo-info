## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:1a6e92987470539f9cb39a033dc3125fa4639a3151f68e8d1159d966e296f90f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e154e8e4461a71aca4a684badb7b226353aad59b3d252e77b9d1410ba291032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244159460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085b3bb9490740c1b2615043d7ae38e90a084208d59d76b8127ae870d3941234`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1c129d6b98b79ca005a42464614c1d43f366795c13f99a7036971861bbc289`  
		Last Modified: Thu, 17 Oct 2024 01:13:29 GMT  
		Size: 145.5 MB (145549908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47455f21edb0f8c8e0c8b032a34a5aa68ded030811f3f5c957cf2f283afdd5f`  
		Last Modified: Thu, 17 Oct 2024 01:13:28 GMT  
		Size: 69.5 MB (69482621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb130e22ea74b077ae25bc5e32698133562175e83299cc9f4ff303acfde54904`  
		Last Modified: Thu, 17 Oct 2024 01:13:27 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5a55cb2cb3ed3505290a9e164cc49cbe9fc8c3f4e860e37adf3a65478e7e7a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8f13ec31727d3c4d3c96dd98367ac096d581b25e9db56563e0caeca41b91d5`

```dockerfile
```

-	Layers:
	-	`sha256:3c44befbd4e9716bd537df5cae04ec2e2580abfc8e1951dc26d7800fe9dd3b38`  
		Last Modified: Thu, 17 Oct 2024 01:13:27 GMT  
		Size: 4.9 MB (4915018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4257b86b3f2415845b002aa69d2dc546604c1ded308e8dcd05910fd33a23823`  
		Last Modified: Thu, 17 Oct 2024 01:13:27 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2f582ac58f5b1e13af86eec3b5ffb2ae2b905d530caad94cc6c5efcfdb35c937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240858753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddc538a9cca111768e890ddabc14eda9d3a75093af18f5c1df78d5b53e069aa`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662b0994744e7d6c9bde45715804f3f36db580397e646e1a9829c0c74993c63`  
		Last Modified: Thu, 17 Oct 2024 08:04:46 GMT  
		Size: 142.4 MB (142356523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637de206af550fd71e790b531751f6564c3b4422a4765d588ab435d6b71d393a`  
		Last Modified: Thu, 17 Oct 2024 08:08:37 GMT  
		Size: 69.3 MB (69345246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c44eae8e292ec3a59005ebfb65966f2123594a41002e8523b3e3bac9e893b6`  
		Last Modified: Thu, 17 Oct 2024 08:08:34 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:03d7b84dee5a5653ece0c78ea6e8063271984f808222fde3e4ee42745558cfba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e3c18ced38c299913a1c51af32e72c9459de522fdfb2f93589d7236c7cf675`

```dockerfile
```

-	Layers:
	-	`sha256:1a999d849503dd0f4e11772f75de463155b7ff855861bd4911f8e2bf11ce4057`  
		Last Modified: Thu, 17 Oct 2024 08:08:35 GMT  
		Size: 4.9 MB (4921403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fdd1d343842aed43806a79d362c35c8f85e94f91c03c9cea3e6dab7f1428ce`  
		Last Modified: Thu, 17 Oct 2024 08:08:35 GMT  
		Size: 14.1 KB (14081 bytes)  
		MIME: application/vnd.in-toto+json
