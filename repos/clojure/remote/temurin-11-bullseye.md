## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:db71c468a73a9fc2c727a0f078d384647739edf9fdcc682fb283e9cc0eea2609
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0d50bec73a4d6320ab6084ef3b16c83dd73aa039d22ae8da982d91a7d4f30d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (269965793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a405a0d83eeb2f7cf5315daa762795fd72df82f7c94f55ae7c3ebe6d7ad86a`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf59bd2fe2dc43935849f1a396d4db734be9fcff4491a4c729029853e3ae6`  
		Last Modified: Wed, 16 Oct 2024 16:13:11 GMT  
		Size: 145.5 MB (145549911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79792dd15a6ca736e2c8cdc9caa504621fb41bda4bc985b4ad6a6045d188baa0`  
		Last Modified: Wed, 16 Oct 2024 16:13:10 GMT  
		Size: 69.3 MB (69333846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa553185be6e1aa99cfd3bd98bac32e9b1f55def6b69574b2bd558390a115d5`  
		Last Modified: Wed, 16 Oct 2024 16:13:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:55b6699e1f3a9cda8b09f279c3a18b95664aade89d494dbe4c00462c2641e8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7224073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d27b099bfa9c642171c54234f187c373e852cb7b4210191bd09a6cc5b1bcf3`

```dockerfile
```

-	Layers:
	-	`sha256:ae96abaebbe112b7d0acd79a348b6282b0674430c5cf767e937a054457212421`  
		Last Modified: Wed, 16 Oct 2024 16:13:08 GMT  
		Size: 7.2 MB (7210170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5897a28cfee29c18d8109ecebd8bc26ee9363e9dd7df7e7091703b3fef77f0a4`  
		Last Modified: Wed, 16 Oct 2024 16:13:07 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:45c958f9a551564608d2471f96ed7e83aa4cafb5edcdc8a2c5ad89ccc29771b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265557911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103843ef37b723bccdd28b1158c0d7e06ca58dc53ae4de5db0bac2db239fb575`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
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
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fda9f9a3b84e45b218f27093a63f7c05ff4fa2dc477dd87cf53ce6b97d2062`  
		Last Modified: Wed, 16 Oct 2024 02:13:38 GMT  
		Size: 142.4 MB (142356484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22547171eb94f8d054aa49d6e53ac08a1e980d57da7fa656c936d5fa1315815`  
		Last Modified: Wed, 16 Oct 2024 02:18:13 GMT  
		Size: 69.5 MB (69466916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1e585038db54f10fd02496891b5cddf361dcca55ae07ae501717540fc257c7`  
		Last Modified: Wed, 16 Oct 2024 02:18:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c9594b629b32144f9ed4d662daf655b3182d4c13e0f29f1e9fa3f064f29c6454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379b56654b41a614c2ac6a75798e0511ee3ed5142203cbef01a29d847b687de1`

```dockerfile
```

-	Layers:
	-	`sha256:19b2cda34827a98f98778dce88b0dd1843ac4bdc75f846e269e76362a1727675`  
		Last Modified: Wed, 16 Oct 2024 02:18:08 GMT  
		Size: 7.2 MB (7215892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47ec09a70bb0ccf3991d43207fc3d155156310d68af7936254ea05f46b3b9bdf`  
		Last Modified: Wed, 16 Oct 2024 02:18:07 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json
