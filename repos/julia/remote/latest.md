## `julia:latest`

```console
$ docker pull julia@sha256:2416b6fdd230c214a4b97e1234456c2360a65318f510a0926c1d8c7e2d290a98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:c1f906f69d2345b75f60d91d6ace270e66571ff4418c6a338edee9775f4d1c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.5 MB (327475956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d631c5a77e45801010967943e4db81bc8ff7b527f04a1a93ea69be586735ecf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:21:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 16 Mar 2026 22:21:43 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:21:43 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 16 Mar 2026 22:21:43 GMT
ENV JULIA_VERSION=1.12.5
# Mon, 16 Mar 2026 22:21:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.5-linux-x86_64.tar.gz'; 			sha256='41b84d727e4e96fbf3ed9e92fa195d773d247b9097f73fad688f8b699758bae7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.5-linux-i686.tar.gz'; 			sha256='aa664f0e5936c7ee2ac093675ea532d33dee60fbb330e62ce45a1a4c4800204a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.5-linux-aarch64.tar.gz'; 			sha256='2e5de844ea4462bfb08a5ba9fa5ae03532183cc0d9e724590e2c8df654f3e8e2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 16 Mar 2026 22:21:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:21:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:21:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782cf41131fe0e1b1e0bad8ad557273cc4ecaee3dc8aa7d4f80942fe3e23744a`  
		Last Modified: Mon, 16 Mar 2026 22:22:28 GMT  
		Size: 6.2 MB (6247016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855e0c20c8139eea184869e05f2b03065426dccc8b3cb01ba4d03872ed4fa7da`  
		Last Modified: Mon, 16 Mar 2026 22:22:46 GMT  
		Size: 291.5 MB (291453073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07f4f51b25ec95bdd84f858ecaa66d301fdd2c0758b92591ee032a2fe07d186`  
		Last Modified: Mon, 16 Mar 2026 22:22:27 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:68b09c3e370cf1418157f52b1a67009cdd95a01b0d34b39cfc35fb9622a094bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8490376e36843ec62a3d89401bedd327c61bda3ec43abb1fab4f801e0a56d5f3`

```dockerfile
```

-	Layers:
	-	`sha256:44854d6d93cfdc3a5d403a2d34031d0212fa3211fc23a4a322efe356aabe5d9c`  
		Last Modified: Mon, 16 Mar 2026 22:22:27 GMT  
		Size: 2.2 MB (2240259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3538d71fc74313ea543190d82f0e08fde626768c047c0d51c2ddb481e21ee70b`  
		Last Modified: Mon, 16 Mar 2026 22:22:27 GMT  
		Size: 17.7 KB (17689 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9256eca73c224f451a5aa3ae3dcf1967a4dce19abd5b59048d8c482de137c3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347546686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be764bd31c0823792f3a88f0c2c1f88023a466a4e4ab832e45218bba34d3436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:21:38 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 16 Mar 2026 22:21:38 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:21:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 16 Mar 2026 22:21:38 GMT
ENV JULIA_VERSION=1.12.5
# Mon, 16 Mar 2026 22:21:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.5-linux-x86_64.tar.gz'; 			sha256='41b84d727e4e96fbf3ed9e92fa195d773d247b9097f73fad688f8b699758bae7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.5-linux-i686.tar.gz'; 			sha256='aa664f0e5936c7ee2ac093675ea532d33dee60fbb330e62ce45a1a4c4800204a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.5-linux-aarch64.tar.gz'; 			sha256='2e5de844ea4462bfb08a5ba9fa5ae03532183cc0d9e724590e2c8df654f3e8e2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 16 Mar 2026 22:21:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:21:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:21:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c71323da8723870fbbfddfcd9665c0e22b21e287e19cb174d21dd2dbc929cce`  
		Last Modified: Mon, 16 Mar 2026 22:22:24 GMT  
		Size: 6.2 MB (6154404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e0b94f71448e8cc3106c016bc494dc97416412481e7c99ae0cba91a1e7071c`  
		Last Modified: Mon, 16 Mar 2026 22:22:29 GMT  
		Size: 311.3 MB (311253497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f02f8cfee60c3df95752cf1f0346657e49f240df2ae9db578b8d8b335c22173`  
		Last Modified: Mon, 16 Mar 2026 22:22:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:e3caad9bec6276e0962e681d04a12d6b1bbc5f929ff524ce1abb43c8212659db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87a068948fa9e96b6165bc2bf9b81e96635c773f77708c1a9d08830d328397f`

```dockerfile
```

-	Layers:
	-	`sha256:cdd2ce5343edca5c83831c63b3b9cfdd3a5da1ade2902de77246e99881b50f1b`  
		Last Modified: Mon, 16 Mar 2026 22:22:23 GMT  
		Size: 2.2 MB (2240591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de72b82b6da10599efe81b3c0a067186967089d13ae8a0063aade15a53f552c8`  
		Last Modified: Mon, 16 Mar 2026 22:22:23 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:4887bde43f99b2ab4fc3209a4aac7247e3561ff79d860d852a597ab7126c320d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268933387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3241cc6f31671b63515c914142820a913ce56a270737e6290ead4d3ec85bc132`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:17:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:17:59 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 16 Mar 2026 22:17:59 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:17:59 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 16 Mar 2026 22:17:59 GMT
ENV JULIA_VERSION=1.12.5
# Mon, 16 Mar 2026 22:17:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.5-linux-x86_64.tar.gz'; 			sha256='41b84d727e4e96fbf3ed9e92fa195d773d247b9097f73fad688f8b699758bae7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.5-linux-i686.tar.gz'; 			sha256='aa664f0e5936c7ee2ac093675ea532d33dee60fbb330e62ce45a1a4c4800204a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.5-linux-aarch64.tar.gz'; 			sha256='2e5de844ea4462bfb08a5ba9fa5ae03532183cc0d9e724590e2c8df654f3e8e2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 16 Mar 2026 22:17:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:17:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:17:59 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4188a191201d27b2fd6df33718d317a42480a2527e1215e43b666d9ce3dcd856`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 6.4 MB (6433738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467af3464334ff31096e0640ff00cac9b83ff9eecd7bdfd095ed991ce18e5057`  
		Last Modified: Mon, 16 Mar 2026 22:18:35 GMT  
		Size: 231.2 MB (231208147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5060914437f078cd6b8cc8afc039ff454f55e62325cf4ba50b8768c8f489eb`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:12048d0490b6aec4e4e11e03c7c05aa855a9c6f6e30a42e6325cb4e2d2f0c670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c05211f91e26d8e6409a9cb1571d57bfc12de7dbd7b94bf0a6b8c4f5f1b8a2`

```dockerfile
```

-	Layers:
	-	`sha256:9129ae638ffaf9bf62708d34fb8509b571567113eb28f418dc3d8a07d37d8177`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 2.2 MB (2237384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa8b57881f9d10f412770ae6f1a7c28a14c597bfbb31616c32459e6bfa98b742`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 17.6 KB (17635 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.26100.32522; amd64

```console
$ docker pull julia@sha256:65013ddff653fc523196484c9a39da356f882ade314e5cc99e5b6a26da46b97b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2367496845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0bc3ce791078c2f28574ea57bae5862141cab5f5ba398e121b7b60eb281820`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 10 Mar 2026 21:57:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 21:57:53 GMT
ENV JULIA_VERSION=1.12.5
# Tue, 10 Mar 2026 21:57:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.5-win64.exe
# Tue, 10 Mar 2026 21:57:55 GMT
ENV JULIA_SHA256=97c0cff9770baa823d40eb6f4f47fdfdcc3c48c609882354c01734f8abcd14f8
# Tue, 10 Mar 2026 21:59:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 10 Mar 2026 21:59:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbcf8b89861397ecd3c383648ae26361b4bbc6542eb69b5505bd750456cd6cda`  
		Last Modified: Tue, 10 Mar 2026 21:59:23 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb6ec51ada248f23da4f30b0954776fa18de33bcdf1731d3913cfd54f7298a4`  
		Last Modified: Tue, 10 Mar 2026 21:59:22 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d86f980b6c8339a206bcfb81e123d7b23efad2003ed398f90d922c413096995`  
		Last Modified: Tue, 10 Mar 2026 21:59:22 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b7f7302f835adb4d8568d532f1e379a7488ccf3d1a54d817819b2d3645d012`  
		Last Modified: Tue, 10 Mar 2026 21:59:22 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ffd7e7209439f26dc1a4619081fe53e33e81734c10fc292ac90fa927e19126`  
		Last Modified: Tue, 10 Mar 2026 22:00:03 GMT  
		Size: 286.3 MB (286294258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2367d1a9bf805d89bef1a738657a6035b4fc694f8c30f13f552a6d9fecac06`  
		Last Modified: Tue, 10 Mar 2026 21:59:22 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.4893; amd64

```console
$ docker pull julia@sha256:2523df2fefc3cdac6b1ca4d80d4a3eb4006b94691b8ecb3ffa086db506389ae0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268662971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddfd09b82167aae284fb3e985932aac5b91ea9bb088012ffb40532090629e44`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:57:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 21:57:06 GMT
ENV JULIA_VERSION=1.12.5
# Tue, 10 Mar 2026 21:57:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.5-win64.exe
# Tue, 10 Mar 2026 21:57:09 GMT
ENV JULIA_SHA256=97c0cff9770baa823d40eb6f4f47fdfdcc3c48c609882354c01734f8abcd14f8
# Tue, 10 Mar 2026 22:00:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:00:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f982b44695c6c1cca851e9238aa8eceda2f7522e65a6a1df319239f66b3610fe`  
		Last Modified: Tue, 10 Mar 2026 22:00:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9871a58174f1cd722a0ec3647de218209df0947a187d6981d8979ea2155a0739`  
		Last Modified: Tue, 10 Mar 2026 22:00:29 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625ae8df47e2d602a7ef9b4204dbc089bee63d98012a5b175118a86bfbf5df1b`  
		Last Modified: Tue, 10 Mar 2026 22:00:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43687756026c65610073c0c5750d7c835e0da7feceb97d8600ca91a0924fe8b0`  
		Last Modified: Tue, 10 Mar 2026 22:00:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c591e4c452dfe9f092314df1a9546c6c03bcdaa65289fdf7a39ccc2bdc4bfa9d`  
		Last Modified: Tue, 10 Mar 2026 22:01:13 GMT  
		Size: 286.4 MB (286375022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278d1a6b9d0f22664afcf8ee0b517b7953e96f3fb7cf062854e64343e97d5e47`  
		Last Modified: Tue, 10 Mar 2026 22:00:30 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
