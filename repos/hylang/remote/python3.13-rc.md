## `hylang:python3.13-rc`

```console
$ docker pull hylang@sha256:587ab06585573b27123a6ddeea23bb741c27e74bff5c9081364485dca0e57ac5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `hylang:python3.13-rc` - linux; arm variant v5

```console
$ docker pull hylang@sha256:946124e4b468b61342f8ef2f59a5b562734ddad482ebd46336219bb240bce8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47569067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1173883749665987ec744f0ee914e04584aa54d4aab0e0f06412d5a78bb0a0d6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.13.0rc2
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce6906f09270354c9da0d208b9e4f68a4c0216ab80b49f2adedf4b346418263`  
		Last Modified: Thu, 05 Sep 2024 08:52:37 GMT  
		Size: 3.1 MB (3081873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a29882c3155eb7bbb1a2b1a8e00bebc3f6fc93695627a3c0e9a05222bccef07`  
		Last Modified: Thu, 12 Sep 2024 21:39:32 GMT  
		Size: 11.9 MB (11916244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9174201a10170a0266526831e66578d87150d1aa1385a8f46d68c21db87fdeac`  
		Last Modified: Thu, 12 Sep 2024 21:39:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af200c0d3f6536882ae10dd31bbedd4a049f7645e6ac33a8f19bd3801bb3173`  
		Last Modified: Tue, 24 Sep 2024 01:07:28 GMT  
		Size: 5.7 MB (5683289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-rc` - unknown; unknown

```console
$ docker pull hylang@sha256:4a7401f91aa9ae09a561dcc6d412b97c788fcd96f76eb165490c22ec239b0928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2423856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dc993e2a946c3567a9af086bc378c7c7427dad7920e19d37212540866a6af8`

```dockerfile
```

-	Layers:
	-	`sha256:7bf3fc8512dafe88e16a7d00ed80e02d445e004820f0c91f9b1516dfbd34a311`  
		Last Modified: Tue, 24 Sep 2024 01:07:28 GMT  
		Size: 2.4 MB (2414526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:459a94e4c7d6f886bdc68b19a6f1d4ba57bd7dd00ea831ec2cdfe1d808b5fdfa`  
		Last Modified: Tue, 24 Sep 2024 01:07:27 GMT  
		Size: 9.3 KB (9330 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-rc` - linux; 386

```console
$ docker pull hylang@sha256:4739f1ea9bf2525fa871968258cb12b20137a1f92aa8b748c345bd249940c288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51879135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9b12dd0f2afa371869c7829b32691c828707909d5313d4d829c764916bcd2c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.13.0rc2
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e757271c40ecf105cc3518aa2b54774fbb5f1dfae4024c1ec63110faff169db`  
		Last Modified: Thu, 12 Sep 2024 21:17:20 GMT  
		Size: 3.5 MB (3509595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c53dbba153bee82ae4a7ff0e12492996bf257f0bfcec5094037a50382168f75`  
		Last Modified: Thu, 12 Sep 2024 21:17:20 GMT  
		Size: 12.5 MB (12542211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ced201f83811f9982217995d0ee4ecf0c290126aab89a7c7d54642432b5e7b`  
		Last Modified: Thu, 12 Sep 2024 21:17:20 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e062164404f44cd878f7ef9b1eceab1a96d28d39a0e026b34ab0d4079cf1c09d`  
		Last Modified: Tue, 24 Sep 2024 01:02:41 GMT  
		Size: 5.7 MB (5682785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-rc` - unknown; unknown

```console
$ docker pull hylang@sha256:4df10ec00051ad0bfeb1cce7c29c22ff9ef5c8b10b9ee9df9c186c94b8b29ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb124026b9b920712dc5ea599a90772104da0969f1cb744d75c6856f78271df`

```dockerfile
```

-	Layers:
	-	`sha256:8c3452667cc050de1f80f47386373e87150246ffbcd4a9cfacdaf3e8a05688bb`  
		Last Modified: Tue, 24 Sep 2024 01:02:41 GMT  
		Size: 8.9 KB (8938 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-rc` - windows version 10.0.20348.2700; amd64

```console
$ docker pull hylang@sha256:cc10dd654b4526d82b92d7473246e5f311fe3a12462f00a9eaa64e2f05669cdc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1530125973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb9b613cb0da81088fe3f4ef49cc84572692760abffe35fc4eceb38d65953c0`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 12 Sep 2024 21:08:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Sep 2024 21:08:21 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 12 Sep 2024 21:08:22 GMT
ENV PYTHON_VERSION=3.13.0rc2
# Thu, 12 Sep 2024 21:09:33 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 12 Sep 2024 21:09:33 GMT
CMD ["python"]
# Tue, 24 Sep 2024 01:03:03 GMT
ENV HY_VERSION=1.0.0
# Tue, 24 Sep 2024 01:03:04 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 24 Sep 2024 01:04:05 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 24 Sep 2024 01:04:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fb02669e1c7a7c5c299e3860b307a51f514d4607cccb978a00ed5a89f9f8f0`  
		Last Modified: Thu, 12 Sep 2024 21:09:36 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76f2596d1965bedcc8f6f1cec27181875a54b0cd1ecbc515a8452e204c78727`  
		Last Modified: Thu, 12 Sep 2024 21:09:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df128227eb9d381fd2041cd713db2074be7cde2f15426b5aea816418c4a446e`  
		Last Modified: Thu, 12 Sep 2024 21:09:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1868a18ba69e19b7aac03f63288067a759a29ec4a363b4dff734300d94f33242`  
		Last Modified: Thu, 12 Sep 2024 21:09:40 GMT  
		Size: 59.1 MB (59066041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbc747e898cfb45be2a972b2ea5d8c227822126bef3d2224a47fb4a77ce26a3`  
		Last Modified: Thu, 12 Sep 2024 21:09:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5428141648305c4c70913eff4ac7411c1aa60a23cd720d6646718270ef90635`  
		Last Modified: Tue, 24 Sep 2024 01:04:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d3cef2376250b66471154604fcae7cd3829b7438696825fcbc2c0fa5754379`  
		Last Modified: Tue, 24 Sep 2024 01:04:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9f79a31d0fa3c3a6f610e370c62f2612d942793e6d58a0443d0796f3949c22`  
		Last Modified: Tue, 24 Sep 2024 01:04:11 GMT  
		Size: 8.9 MB (8858504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccad436a2a915d482b98ec66b4a109ca126871bc0fa8d6c02aa7a1e24a29a9dd`  
		Last Modified: Tue, 24 Sep 2024 01:04:09 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.13-rc` - windows version 10.0.17763.6293; amd64

```console
$ docker pull hylang@sha256:a291729075db35174df97930f05586c0d72625a6e7f05e1bf7714b6544004535
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1784927338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5625c77265a3d27c717726e0d3fa0d9f72df2ad760ece64d4a083711c32ba49d`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 12 Sep 2024 21:09:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Sep 2024 21:09:31 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 12 Sep 2024 21:09:31 GMT
ENV PYTHON_VERSION=3.13.0rc2
# Thu, 12 Sep 2024 21:11:09 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 12 Sep 2024 21:11:10 GMT
CMD ["python"]
# Tue, 24 Sep 2024 01:02:30 GMT
ENV HY_VERSION=1.0.0
# Tue, 24 Sep 2024 01:02:32 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 24 Sep 2024 01:04:11 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 24 Sep 2024 01:04:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6d3d9c27db4b5742e09a7b962be5361ac168e00db52f1c263461c327a7ef42`  
		Last Modified: Thu, 12 Sep 2024 21:11:13 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e3b1062555592ce5b3d2ccd31cf74e536b56851e64b5c76b4b03b2190b1663`  
		Last Modified: Thu, 12 Sep 2024 21:11:13 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5734031cfd6d458eafa3232373f9ca4d0c47a0bd2dc2bcfaf9ec956a3c651cae`  
		Last Modified: Thu, 12 Sep 2024 21:11:13 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d069e2351f91c3730d3ff2070ec88a2d777b074e085ad382e99e2eb158348f02`  
		Last Modified: Thu, 12 Sep 2024 21:11:18 GMT  
		Size: 57.5 MB (57463524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc179a51325e9c2fae3941776192fc30e30f8e24abd00b655f47f222c431b564`  
		Last Modified: Thu, 12 Sep 2024 21:11:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15065744830619527e87184c8a3e0b3191c3499fe8cd24800c511fdbafe503ab`  
		Last Modified: Tue, 24 Sep 2024 01:04:14 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e9c9643049e42306d9501dc6ae403608371925493131b40b86c0957db15f0b`  
		Last Modified: Tue, 24 Sep 2024 01:04:14 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9b6d467bef70f272c981e20dc28457cc1e17f4df9ffdb6951ab1f375e4088a`  
		Last Modified: Tue, 24 Sep 2024 01:04:15 GMT  
		Size: 7.2 MB (7186322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d6786e083f0d691fcf010b99823cece4a121e602dd81e69b2e8cee496726e`  
		Last Modified: Tue, 24 Sep 2024 01:04:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
