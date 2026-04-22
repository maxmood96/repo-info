## `sapmachine:21-jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:e01374ccfd2782c4a6d4d81eb6ea60220442f05c2e4d54a93b9518746533bb24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:795da2b8c3fe2cdc16106d33eb8d827cd600585b4aef841cb10abf0788a865b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64732280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deadc78fbe1a195946f40be068e275322783361c14506e64cdaf8ad19a3488c2`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:04:55 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jre=21.0.11-r0 # buildkit
# Tue, 21 Apr 2026 23:04:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jre
# Tue, 21 Apr 2026 23:04:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ca58d0cdda1a4664c0f739ca2ff42926c83b10db1b76f58ad0b238bdab6bfc`  
		Last Modified: Tue, 21 Apr 2026 23:05:08 GMT  
		Size: 60.9 MB (60924091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:67aa6ee6680fccccc66e85fedfb79fdacd9fb721e6e46d02329793a5528e24b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.2 KB (434225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd352633255feed1495f14858e4541d237bf4a5667b7360b23610b37b85d87e`

```dockerfile
```

-	Layers:
	-	`sha256:5edda14af63c4da10f94c88fc14287854dcae176b346abdd45474af9dca83f62`  
		Last Modified: Tue, 21 Apr 2026 23:05:06 GMT  
		Size: 427.3 KB (427265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a5644c4b383df8098e698ee703720105710cdda562a257dc1ec91884f76628`  
		Last Modified: Tue, 21 Apr 2026 23:05:06 GMT  
		Size: 7.0 KB (6960 bytes)  
		MIME: application/vnd.in-toto+json
