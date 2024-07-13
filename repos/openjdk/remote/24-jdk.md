## `openjdk:24-jdk`

```console
$ docker pull openjdk@sha256:ff867dcec1eb16f20401079b66ddc5686b4e241ad6c49113c9582b653a27aebf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `openjdk:24-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:b35661af838fd678573ed7a908915ece18eba919fd9cdfe66ef6521a68a46133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298372271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9ab2bd8f6cc05811e18d68873ffa8b12ddba5e3ed97bbb84eafac2d40c268f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 12 Jul 2024 06:52:24 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_VERSION=24-ea+6
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='85969884f11f2863595c13dff1cb6f6d94149bbe5188c34f0a7aaa284a545a27'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c719648382b7e5d564dc1d39d4408890d92ce5484fd46a5ef338da7380684ca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8248cefd8100d93cb09342af6b39f9d587c5b357f310f33d264ae0cae561eb62`  
		Last Modified: Fri, 12 Jul 2024 21:57:24 GMT  
		Size: 37.9 MB (37872104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2607ce261146b862a675d659da86bd460bee43b12ad00b4e1946610ff1445d`  
		Last Modified: Fri, 12 Jul 2024 21:57:27 GMT  
		Size: 211.5 MB (211506431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:9b5c3df36b60699bfa334e53400a8f61425801bdf671aab2ddc93c3370fb776a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4dbbd932830ef702b9a5ffef939c508fb981df9ee3506886993f884732ccb5`

```dockerfile
```

-	Layers:
	-	`sha256:72a23e2052672b35ff321b2b730b1aef1f906e7b8d6729fa33db4e520002d4ce`  
		Last Modified: Fri, 12 Jul 2024 21:57:24 GMT  
		Size: 3.3 MB (3333228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f54b80a64657d6c5f3ea776081327024882aca2fd1f55fe181e1b5005bff30dd`  
		Last Modified: Fri, 12 Jul 2024 21:57:23 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0244b120a66df5f3d364e78f6080a739e3a3a15efbe6cab190b21d0858737050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295300597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0988b7857836516ed61f05f46ad591f1908a18af049b2850bd1d05ce724902`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 22:40:25 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Mon, 08 Jul 2024 22:40:26 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 12 Jul 2024 06:52:24 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_VERSION=24-ea+6
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='85969884f11f2863595c13dff1cb6f6d94149bbe5188c34f0a7aaa284a545a27'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c719648382b7e5d564dc1d39d4408890d92ce5484fd46a5ef338da7380684ca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3129baf21359e4eb83f9d1391c216edfe6dce92354dbd70df14232415144a124`  
		Last Modified: Fri, 12 Jul 2024 22:04:48 GMT  
		Size: 38.3 MB (38259249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3cc192964be46952701da1855f6d030aafa73ac193e55b5fcf67cfe1d85af`  
		Last Modified: Fri, 12 Jul 2024 22:04:52 GMT  
		Size: 209.4 MB (209388687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:1d12505812136033fb1da564bf5f8d8dce0a22141ba8625e6b4ea5ef31388a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67111f951c8d96df20acf102ccd1ff031601a74a64b3754835aab1feff4d9695`

```dockerfile
```

-	Layers:
	-	`sha256:f22608b80d9a6e2dc485072af5481fc5c5c3e276ff4c5e978a23e9491a063da0`  
		Last Modified: Fri, 12 Jul 2024 22:04:47 GMT  
		Size: 3.3 MB (3331611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93aa333c100c60423b5a9b92a5d30504a00f86992987a30d162fd7e9d78acf2a`  
		Last Modified: Fri, 12 Jul 2024 22:04:47 GMT  
		Size: 20.0 KB (19977 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - windows version 10.0.20348.2582; amd64

```console
$ docker pull openjdk@sha256:0a65355883750200cc3e8e16e4314027b276538e6f8a24fbd11c40fb7bf68162
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2347036012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252c3452a87ca673fc18c784ba9d66898e3618e84f90a244e351902c3a92e66c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Fri, 12 Jul 2024 22:07:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Jul 2024 22:08:15 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:08:16 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 12 Jul 2024 22:08:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:08:22 GMT
ENV JAVA_VERSION=24-ea+6
# Fri, 12 Jul 2024 22:08:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_windows-x64_bin.zip
# Fri, 12 Jul 2024 22:08:23 GMT
ENV JAVA_SHA256=de012f73dcdc78f7014626b96cb7a381e0bed5be0c8ffac72b7be101bf3d3087
# Fri, 12 Jul 2024 22:08:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:08:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cdef924f34b87fac9d081e881d5e30661c9ca17abd9889d3cbd16e51b55318`  
		Last Modified: Fri, 12 Jul 2024 22:08:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a9e7fd4bd5bb36d2de8797866aea104415fc33c343103bd243cbcf9c749d92`  
		Last Modified: Fri, 12 Jul 2024 22:08:48 GMT  
		Size: 371.6 KB (371574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cd4e919c0b61bbe3e9a6b040da1951a4f12c5725b5a6b53d161d8900ba7549`  
		Last Modified: Fri, 12 Jul 2024 22:08:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052c3ef8d7b597e56a45635bf0ee70f053c64814c7edda28501dea69445d4997`  
		Last Modified: Fri, 12 Jul 2024 22:08:48 GMT  
		Size: 356.1 KB (356139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582eb1fbe26795aba53e7144f8a0f62b51b609e0f9c2bc352c4702cd78905519`  
		Last Modified: Fri, 12 Jul 2024 22:08:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e41ef539c1f30af22ee3c64c9bf48227076e34248abf7a6c68380f4259292f8`  
		Last Modified: Fri, 12 Jul 2024 22:08:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0202cbc27c97abfc59dbd69a2d104d1f2523c7d486f7abab35848e6ee51979da`  
		Last Modified: Fri, 12 Jul 2024 22:08:46 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85be59bfdfb316aa676fb2d5f1649936e2dec45193f165b226871ceb2d84edac`  
		Last Modified: Fri, 12 Jul 2024 22:08:58 GMT  
		Size: 206.7 MB (206700265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aea13824e6699eafe333d2f94ca11db76d993d13acde4ad6e3126f84b2544d`  
		Last Modified: Fri, 12 Jul 2024 22:08:46 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-jdk` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:bad1f6ac2846221753d2a79ee8f0c5d3a298bdb38cb0abc69e379520e899a549
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2445995343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de3ec1e5e9b0ddf64759e4635e4a15be2919ee73974f3e52970ef699a3be4fa`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Fri, 12 Jul 2024 22:03:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Jul 2024 22:03:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:03:46 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 12 Jul 2024 22:04:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:04:07 GMT
ENV JAVA_VERSION=24-ea+6
# Fri, 12 Jul 2024 22:04:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_windows-x64_bin.zip
# Fri, 12 Jul 2024 22:04:08 GMT
ENV JAVA_SHA256=de012f73dcdc78f7014626b96cb7a381e0bed5be0c8ffac72b7be101bf3d3087
# Fri, 12 Jul 2024 22:04:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:04:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8210e664feb4e49050207342f308e57bd9313628e7f5ecd4b96af6e978e4a2cb`  
		Last Modified: Fri, 12 Jul 2024 22:04:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461e07c02594a007b4189bc75fc436b2a422d246fa68c26242d00d8137a05eb2`  
		Last Modified: Fri, 12 Jul 2024 22:04:52 GMT  
		Size: 500.5 KB (500505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33eeb845dd4936fc59d99909d9ebc896fa747196ebeafd3d4ba4b31fb31245e2`  
		Last Modified: Fri, 12 Jul 2024 22:04:52 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7b969ab974fabdaab3c6448f16321d185a6babcfe6a985303732b8f448e6cc`  
		Last Modified: Fri, 12 Jul 2024 22:04:52 GMT  
		Size: 352.3 KB (352310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a004f59a138cc09747e2231381eecfff5dd53f91a2400cf6cd240be33d785c7`  
		Last Modified: Fri, 12 Jul 2024 22:04:50 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fee3ff0299a8f7734a063d93c3900112be3fd8cb0bbb3d17b752f932bdb731`  
		Last Modified: Fri, 12 Jul 2024 22:04:50 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c2b246cff612e872efbb8fd62765781c17e24db220d2918f4aae12d03550cb`  
		Last Modified: Fri, 12 Jul 2024 22:04:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c30e0584e11e63e70e31f7c9caf0c001c324e94602e539593d6f8e0d07716ce`  
		Last Modified: Fri, 12 Jul 2024 22:05:06 GMT  
		Size: 206.7 MB (206705377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9eb3c53fbbbb3f1248b66db22f31b84c8245c3a4dbe08ba00dd6c9c43631de7`  
		Last Modified: Fri, 12 Jul 2024 22:04:50 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
