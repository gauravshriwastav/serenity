PROGRAMS = TestString TestQueue TestVector TestHashMap TestJSON TestWeakPtr TestNonnullRefPtr TestRefPtr TestFixedArray TestFileSystemPath TestURL TestStringView

CXXFLAGS = -std=c++17 -Wall -Wextra -ggdb3 -O2 -I../ -I../../

SHARED_TEST_OBJS = \
	../String.o \
	../StringImpl.o \
	../StringBuilder.o \
	../StringView.o \
	../LogStream.o \
	../JsonArray.o \
	../JsonObject.o \
	../JsonValue.o \
	../JsonParser.o \
    ../FileSystemPath.o \
    ../URL.o \

.cpp.o:
	@echo "HOST_CXX $<"; $(PRE_CXX) $(CXX) $(CXXFLAGS) -o $@ -c $<

define execute-command
$(1)

endef

all: $(PROGRAMS)
	$(foreach x,$(PROGRAMS),$(call execute-command,./$(x)))

TestString: TestString.o $(SHARED_TEST_OBJS)
	$(PRE_CXX) $(CXX) $(CXXFLAGS) -o $@ TestString.o $(SHARED_TEST_OBJS)

TestQueue: TestQueue.o $(SHARED_TEST_OBJS)
	$(PRE_CXX) $(CXX) $(CXXFLAGS) -o $@ TestQueue.o $(SHARED_TEST_OBJS)

TestVector: TestVector.o $(SHARED_TEST_OBJS)
	$(PRE_CXX) $(CXX) $(CXXFLAGS) -o $@ TestVector.o $(SHARED_TEST_OBJS)

TestFixedArray: TestFixedArray.o $(SHARED_TEST_OBJS)
	$(PRE_CXX) $(CXX) $(CXXFLAGS) -o $@ TestFixedArray.o $(SHARED_TEST_OBJS)

TestHashMap: TestHashMap.o $(SHARED_TEST_OBJS)
	$(PRE_CXX) $(CXX) $(CXXFLAGS) -o $@ TestHashMap.o $(SHARED_TEST_OBJS)

TestJSON: TestJSON.o $(SHARED_TEST_OBJS)
	$(PRE_CXX) $(CXX) $(CXXFLAGS) -o $@ TestJSON.o $(SHARED_TEST_OBJS)

TestWeakPtr: TestWeakPtr.o $(SHARED_TEST_OBJS) 
	$(PRE_CXX) $(CXX) $(CXXFLAGS) -o $@ TestWeakPtr.o $(SHARED_TEST_OBJS)

TestNonnullRefPtr: TestNonnullRefPtr.o $(SHARED_TEST_OBJS)
	$(PRE_CXX) $(CXX) $(CXXFLAGS) -o $@ TestNonnullRefPtr.o $(SHARED_TEST_OBJS)

TestRefPtr: TestRefPtr.o $(SHARED_TEST_OBJS)
	$(PRE_CXX) $(CXX) $(CXXFLAGS) -o $@ TestRefPtr.o $(SHARED_TEST_OBJS)

TestOptional: TestOptional.o $(SHARED_TEST_OBJS)
	$(PRE_CXX) $(CXX) $(CXXFLAGS) -o $@ TestOptional.o $(SHARED_TEST_OBJS)

TestFileSystemPath: TestFileSystemPath.o $(SHARED_TEST_OBJS)
	$(PRE_CXX) $(CXX) $(CXXFLAGS) -o $@ TestFileSystemPath.o $(SHARED_TEST_OBJS)

TestURL: TestURL.o $(SHARED_TEST_OBJS)
	$(PRE_CXX) $(CXX) $(CXXFLAGS) -o $@ TestURL.o $(SHARED_TEST_OBJS)

TestStringView: TestStringView.o $(SHARED_TEST_OBJS)
	$(PRE_CXX) $(CXX) $(CXXFLAGS) -o $@ TestStringView.o $(SHARED_TEST_OBJS)

clean:
	rm -f $(SHARED_TEST_OBJS)
	rm -f $(PROGRAMS)
