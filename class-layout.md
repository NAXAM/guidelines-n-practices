
# Class layout
This describes how a pratical class will be layout and looked like.

Overral idea: class members will be
- grouped by type and groups orderred as the listed below
    - Constant fields
    - Static Readonly fields;
    - Static method
    - Event
    - Property
    - Field
    - Constructor
    - Method
    - Command
- orderred by access modifier
    - Public
    - Internal
    - Protected
    - Private

NOTE: 
1. In each group, it's preferred to order members alpabetically.
2. In particular project, we might group members by business functionality. However, we should avoid if we could refactor by other way.
3. Property members  must be created by using pre-defined snippets inside VisualStudio or listed in [MVVM Common Snippets](./mvvm-common-snippets.md#common-blocks)

```c#
namespace Naxam.Practices {
    class SampleClass {
        public const string StaticReadOnlyPublicField;
        protected const string StaticReadOnlyProtectedField;
        const string staticReadOnlyPrivateField;

        public static readonly string StaticReadOnlyPublicField;
        protected static readonly string StaticReadOnlyProtectedField;
        static readonly string staticReadOnlyPrivateField;

        public static void StaticPublicMethod() {}
        protected static void StaticProtectedMethod() {}
        static void StaticPrivateMethod() {}

        public event EventHanlder PublicEvent;
        protected event EventHanlder ProtectedEvent;
        event EventHanlder PrivateEvent;

        public string PublicProperty { get; set; }
        string _PublicPropertyWithBackingField;
        public string PublicPropertyWithBackingField { 
            get => _PublicPropertyWithBackingField; 
            set => _PublicPropertyWithBackingField = value; 
        }
        protected string ProtectedProperty { get; set; }
        protected string protectedField;
        protected readonly string protectedReadonlyField;
        string privateField;

        public SampleClass(string arg1, string arg2) {}
        public SampleClass(string arg1) {}
        public SampleClass() {}

        public string MethodPublic() {}
        protected string MethodProtected() {}
        string MethodPrivate() {}

        ICommand _NameCommand;
        public ICommand NameCommand => (_NameCommand = _NameCommand ?? new Command<object>(ExecuteNameCommand, CanExecuteNameCommand));
        bool CanExecute$name$Command(object parameter) { return true; }
        void Execute$name$Command(object parameter) {}
    }
}
```