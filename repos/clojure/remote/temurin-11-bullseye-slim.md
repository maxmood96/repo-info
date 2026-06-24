## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:203afd7e7d0ad8a1150c715dd6ee6d62e39f130d5f1740de436eb7180309c557
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b3116ed16e490e8d71bd42173a1de6413e1ac195dcf91ee349b293aae8fab8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232246824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef0965e4b9961ff26f2c89e5fca49226d61233ee9c21129d95155b8d1064f11`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:17:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:17:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:17:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:17:05 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:17:05 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:17:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:17:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:17:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0251c4232e4025b51352f0bb7119fd866d4a6a62861f09baea6fe5af4c6eee59`  
		Last Modified: Wed, 24 Jun 2026 00:28:14 GMT  
		Size: 30.3 MB (30259447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a5cc9ad15efd496b3d6f6f83bc99ee145b69e35355e4adab8aa28b24d02ca8`  
		Last Modified: Wed, 24 Jun 2026 02:17:42 GMT  
		Size: 145.9 MB (145886224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288814ee35084324ae256240a886bab6871b3c13d1ad651b56fe16f30952d97d`  
		Last Modified: Wed, 24 Jun 2026 02:17:39 GMT  
		Size: 56.1 MB (56100509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e72537e49981ea80f55be553a5ce1ca152300f32972638267f12f7ae5e1ffe2`  
		Last Modified: Wed, 24 Jun 2026 02:17:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3973f22a4d3e6d6445b0ae78c1d5b7c11f0e2471a6bf6c4663b368bec4ca7819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5351785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7834a04c9a9469249e438e3f8f45d5833a11f594ce61a92528d44df44d455d`

```dockerfile
```

-	Layers:
	-	`sha256:e5039030f73fbef9d1f6388ccaa4bda14ecfef91cc57e8cabfd1ed6775c8828d`  
		Last Modified: Wed, 24 Jun 2026 02:17:37 GMT  
		Size: 5.3 MB (5337365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee4d89f15db90204a3407f13d543daef9c0484fd8c93e9830241b9b1608f8d0`  
		Last Modified: Wed, 24 Jun 2026 02:17:37 GMT  
		Size: 14.4 KB (14420 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e11a47437ce17665ff74e8af2de3463103c782b815478a9014f705a4c22ab13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227597527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6b817df0c9afd431f243f0fc175f9c2f123d57ddb14eb4a7fc11cba313eed1`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:23:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:23:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:23:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:23:25 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:23:25 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:23:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:23:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:58009b48fe731a10341c4f5f98dfa280afd10fa34cc71961411d37e306120dd0`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 28.7 MB (28746926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da9baeac015be503ca28c87cf58eda300e5f3a06fc6271c374a1b1af3864247`  
		Last Modified: Wed, 24 Jun 2026 02:24:00 GMT  
		Size: 142.6 MB (142582162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46c147ede7cdc1227cbd19ee3c95c73e7b41e3de67f3a8aff50f49a56158d9d`  
		Last Modified: Wed, 24 Jun 2026 02:23:59 GMT  
		Size: 56.3 MB (56267795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a38a7e0e10ec81eac0abfe4d141ce19e871d0ad72284fdb1c7baa9c90e14e6`  
		Last Modified: Wed, 24 Jun 2026 02:23:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:da2fa51f3aa806bbf8c85c3dda9bdb191c4836f1af5c572bba028c6fe68ba6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5358254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f894a52666af2237e68c31f353dedf1244eacd29f74159508e896ba41071763a`

```dockerfile
```

-	Layers:
	-	`sha256:e671f814fa3018f1e3dd497c0f3241e1a7b9a555b7fbc5a3421b2fc0439a80ca`  
		Last Modified: Wed, 24 Jun 2026 02:23:57 GMT  
		Size: 5.3 MB (5343715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:801a169eec08af078ed70b34eaa283f704f0d3116d1cafa8411366bebb37118a`  
		Last Modified: Wed, 24 Jun 2026 02:23:56 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json
