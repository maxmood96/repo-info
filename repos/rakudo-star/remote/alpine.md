## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:b2bd6c9526b339eb3ca3103b098571447f70c6296be183c8e362578e7cf170f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:9eec117e33b1800f007692bc8e82e6a8560365b6feb63e53894df7a5f717f803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48585272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21194f4d0380cfdd55c7c207fe9ce897942316397d9a996551507920cd29585`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 21:11:49 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ARG rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
ENV rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
# ARGS: rakudo_version=2024.09-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 03 Oct 2024 21:11:49 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3128327b77aec3fd403bb2f7463b2edff305d97c91d7a8b722ac38e2bb2990`  
		Last Modified: Sat, 19 Oct 2024 01:13:54 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cfbb22abb757d26c6d46bd02f4587ee31ea93cb42946664bd9de36e2e20dc9`  
		Last Modified: Sat, 19 Oct 2024 01:13:55 GMT  
		Size: 45.0 MB (44960503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:b699f7f0514961b048225d2f5f429f9958de9c61e83094375f4b521324c9693c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 KB (127376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7669ad49f8babedbf2f0dcc5d85d5468f2d2923065aaa0426a801ad5559b4c49`

```dockerfile
```

-	Layers:
	-	`sha256:3ac922819e3554c14292089660b41ae1cf6ed5d204f27e5da1534e6bf5ef3fa8`  
		Last Modified: Sat, 19 Oct 2024 01:13:54 GMT  
		Size: 115.8 KB (115835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:993aef0341f574e539cddf05e52b0e84fedc56dd08f51ee201d5b9a21841def5`  
		Last Modified: Sat, 19 Oct 2024 01:13:54 GMT  
		Size: 11.5 KB (11541 bytes)  
		MIME: application/vnd.in-toto+json

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:f47630391219dcaa6188720c8ba0b64333ea67eaabe19e9ad19b23cf4cb00f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48884392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83be2540b8ee30dfc0178ecc3024c6f6f9523638df179f13b953256a5c5a09e9`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 03 Oct 2024 21:11:49 GMT
RUN addgroup -S raku && adduser -S raku -G raku # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ARG rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
ENV rakudo_version=2024.09-01
# Thu, 03 Oct 2024 21:11:49 GMT
# ARGS: rakudo_version=2024.09-01
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyfp="3E7E3C6EAF916676AC549285A2919382E961E2EE"     pubkeyurl="https://rakudo.org/keys/rakudo_github_automation-${keyfp}.asc"     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="${tmpdir}/gnupg"     && mkdir $GNUPGHOME     && apk add --no-cache --virtual .build-deps $buildDeps     && apk add --no-cache readline     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && wget $pubkeyurl -O ${tmpdir}/key.asc         && gpg --batch --import ${tmpdir}/key.asc     && gpg --batch --export $keyfp > ${tmpdir}/${keyfp}.asc     && rm -rf $GNUPGHOME     && mkdir $GNUPGHOME     && gpg --batch --import ${tmpdir}/${keyfp}.asc     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps # buildkit
# Thu, 03 Oct 2024 21:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 03 Oct 2024 21:11:49 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3710cd6f66dcae21a2ea1d0e6836d71d87df8a4f52edd5e66addc9ae38299c`  
		Last Modified: Sat, 19 Oct 2024 05:09:33 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b82e14b7459207e44e6f82f4747c60b602cc6969958df0c5d7b8b9e06f03932`  
		Last Modified: Sat, 19 Oct 2024 05:09:35 GMT  
		Size: 44.8 MB (44795785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rakudo-star:alpine` - unknown; unknown

```console
$ docker pull rakudo-star@sha256:3bea723533bb6ab131f927edba830709a263e52aceb3e548709f73b952908a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 KB (127498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88897c4e77d87e26c6e8afacfe40e3db590be58e91d2029e731b4a7a6c1f5211`

```dockerfile
```

-	Layers:
	-	`sha256:91267b83f9a7c879fcfa073e2f51a3fcd4ae88668c247bbd8b5e50b6a9ee886a`  
		Last Modified: Sat, 19 Oct 2024 05:09:33 GMT  
		Size: 115.9 KB (115867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496f11f4d0db711be504c58de58df1afd117ce7fe9a63b11a55ea3bd9e3f09d1`  
		Last Modified: Sat, 19 Oct 2024 05:09:33 GMT  
		Size: 11.6 KB (11631 bytes)  
		MIME: application/vnd.in-toto+json
